# Debug
*Tao Zhineng*
## The first little bug(I'm not sure)
In the Lecture-3.md file:
###	Constructor and destructor
#### 3. Is it necessary to declare destructors（析构函数） as public members? What about constructors（构造函数）?

- 析构函数: 不是. 构造函数: 不是.
- 原因：
  - 如果你不想让外面的用户直接构造一个类（假设这个类的名字为`A`）的对象，而希望用户只能构造这个类`A`的子类，那你就可以将类`A`的构造函数/析构函数声明为`protected`/`private`。
  - <mark>如果将构造函数/析构函数声明为`private`，则类的使用者无法构造和这个类的对象</mark>，单件设计模式由此而来：

  ```cpp
  #include <iostream>
  using namespace std;
  
  class A
  {
  private:
      A(): data(10) { cout << "A" << endl; }
      ~A() { cout << "~A" << endl; }
  public:
      static A& Instance()
      {
          static A a;
          return a;
      }
      void Print()
      {
          cout << data << endl;
      }
  private:
      int data;
  };
  int main(int argc, char** argv)
  {
      A& ra = A::Instance();
      ra.Print();
  }
  ```
### explanation:

If we just define the destructor as private and the constructor as default or as public, we can also define an object through the keyword new:
```cpp
#include <iostream>
using namespace std;

class A
{
private:
    ~A() { cout << "~A" << endl; }
public:
    static A& Instance()
    {
        static A a;
        return a;
    }
    void Print()
    {
        cout << data << endl;
    }
private:
    int data;
};
int main(int argc, char** argv)
{
    A *ra=new A();
    ra->Print();
    return 0;
}
```
## the second debug
In the Lecture-5.md file:
### 17.	What are the differences between static and non-static member functions?

- 出现在类体外的函数定义不能指定关键字`static`；
- 静态成员之间可以相互访问，包括静态成员函数访问静态数据成员和访问静态成员函数；
- 非静态成员函数可以任意地访问静态成员函数和静态数据成员；
- 静态成员函数不能访问非静态成员函数和非静态数据成员；
- 由于没有`this`指针的额外开销，因此静态成员函数与类的全局函数相比速度上会有少许的增长；
- 调用静态成员函数，可以用成员访问操作符(`.`)和(`->`)为一个类的对象或指向类对象的指针调用静态成员函数，当同一类的所有对象使用一个量时，对于这个共用的量，可以用静态数据成员变量，这个变量对于同一类的所有的对象都取相同的值。<mark>静态成员变量只能被静态成员函数调用</mark>。静态成员函数也是由同一类中的所有对象共用。只能调用静态成员变量和静态成员函数。
### explanation:
Static member variable can be invoked by other member functions:
```cpp
#include<iostream>
using namespace std;
class abcd
{
public:
	static int MAX_NUM;
	void addoutput();
};
int abcd::MAX_NUM = 100;
void abcd::addoutput()
{
	MAX_NUM++;
}
int main()
{
	abcd a;
	cout << a.MAX_NUM << endl;
	a.addoutput();
	cout << a.MAX_NUM << endl;
	return 0;
}
```

*edit by Typora*