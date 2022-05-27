# Introduction of different C++ editors
*Tao Zhineng*			04/09/2022
# VI
* VI is the standard editor of the system under Unix and Linux systems, founded by Bill Joy at the University of California, Berkeley. The name “VI” is derived from the word "visual“, Because it is intended to edit text on a video terminal with a removable cursor.

* VI is as powerful as any latest text editor. But most Linux systems do not contain real VI, they come with a premium alternative called vim(VI improved).VI and VIM have exactly the same functions. The difference between them is that VIM adds an edit with text color

* VI has three working modes: command mode, insert mode and bottom line mode.

* After opening the file with VI editor, the default mode is command mode. In this mode, you can control the movement of the cursor and the copy, paste, delete and other operations of the text content through the keyboard.
## command mode

### The movement of cursor
| 操作符 |                                          功能                                             |
|:---------:|:--------------------------------------------------------------------------:|
| “上键”或k | 光标上移 |
| “下键”或j | 光标下移 |
| 0和$ | 光标移到行首和行尾 |
| nG | 光标定位到第n行行首 |

### Content deletion
| 操作符 |                                          功能                                             |
|:---------:|:--------------------------------------------------------------------------:|
| x | 删除光标所在的单个字符 |
| dd | 删除光标所在当前行 |
| ndd | 删除光标所在行以及其后n行 |
| d+^ | 删除光标位置到行首内容 |
### Copy and Paste
| 操作符 |                                          功能                                             |
|:---------:|:--------------------------------------------------------------------------:|
| yy | 复制光标所在行 |
| nyy | 复制光标所在行以及其后n行 |
| ygg | 复制光标所在行到首行 |
| yG | 复制光标所在行到页尾 |
### other useful function
* u :revoke
* . :Repeat the last command executed
* J :Merge two lines
* r :Replace the character of the cursor
## insert mode
only in this mode can the content of text be added and modified.
## Last line mode
In the last line mode, you can exit the current editor, save the text, find and save the text content and so on.
### common last line mode commands are as follows:
* set number: :set nu
* set nonumber: :set nonu
* Display control characters: :set list
* No character display control: :set nolist
* Position the cursor on line n: :n
* Keyword seeking: :/…
# EMACS
* Emacs, the abbreviation of“Editor MACroS”(编辑器宏）, was originally completed by Richard Stallman and Guy Steele at MIT in 1975. This idea is inspired by TECMAC and TMACS, which are macro text editors written by guy Steele, Dave moon, Richard Greenblatt, Charles Frankston and others.
* Emacs is not just an editor, it is an integrated environment, or you can call it an integrated development environment.
*√ Send and receiving email 
√ Via Telnet login host View Calendar 
√ Writing article outline 
√ Editing debugging programs for multiple programming languages, combined with GDB, EDebug, etc*

## Editing mode
* Emacs applies the corresponding editing mode to different types of text(i.e. major mode).Emacs defines different major modes for a variety of documents, including normal text files, source files for various programming languages, HTML documents, TEX and LaTeX documents, and other types of text files and so on.
* Each major mode has special Emacs Lisp variables and functions that make it more convenient for users to handle this particular type of text in this mode.For example, the various programmed major modes syntactically highlight the keywords, annotations in the source file text in different fonts, and colors.
* The major mode also provides specially defined commands such as jumping to the beginning or end of a function.
* Emacs can also further define the " minor mode " .Each buffer can be associated with one major mode but multiple minor modes simultaneously.For example, writing a C major mode can define multiple minor modes at once, each minor mode has a different indent style.
# VS code
* Vs Code (short for visual studio code) is a cross platform source code editor running on Mac OS X, windows and Linux for writing modern web and Cloud Applications officially announced by Microsoft at the build Developer Conference on April 30, 2015. Vs code can run on the desktop and can be used for windows, MacOS and Linux. It has access to JavaScript, typescript and node JS, and has rich other languages (such as C + +, C, Java, python, PHP, go) and runtime extended ecosystems (such as. Net and unity).
* The full version of visual studio still runs only on windows and Mac OS.
* The editor also integrates all the features that a modern editor should have, including syntax highlighting, customizable keyboard bindings, bracket matching and snippets. In addition, the editor also has out of the box support for GIT. Microsoft docs provides corresponding learning tutorials to help users log in to GitHub in Visual Studio code.
* Visual studio code provides rich shortcuts.
* The editor supports writing in multiple languages and file formats. As of September 2019, it has supported 37 languages or files.
## The installation of VS code and how to use it
* download and install VS code editor
Download for free on the official website, install according to the guide and decide whether to install Chinese plug-ins.
* Configure system environment variables
Go to https://sourceforge.net/projects/mingw-w64/files/mingw-w64/mingw-w64-release/ to download MinGW and then configure the system environment variable.
* Download C/C + + plug-in and Configure VS code environment variables
You need a new file folder with three files named: c_cpp_properties.json, launch.json, tasks.json(Go to see the reference)
### For installing vs Code on Linux system, you can share folders (if you don't want to use the app store in the virtual machine). See references for the steps. 
Windows:https://blog.csdn.net/weixin_48468423/article/details/118950592?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165119954016782388049459%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165119954016782388049459&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-118950592.142^v9^control,157^v4^control&utm_term=vscode%E9%85%8D%E7%BD%AEc%2B%2B%E7%8E%AF%E5%A2%83&spm=1018.2226.3001.4187
Linux: https://blog.csdn.net/shuiyixin/article/details/98970992
# CLion
* Clion is a cross platform IDE designed for developing C and C + +. It is designed based on IntelliJ and contains many intelligent functions to improve the productivity of developers. This powerful IDE helps developers develop C / C + + on Linux, MAC OS X and windows. 
* The official website calls this IDE a smart C / C + + editor ,its major characteristic function:Code assistance , Code generation , Safe refactoring and Quick Documentation.
## Code assistance
Read and write code effectively with an editor that deeply understands C and C++. Have completion results filtered by type in Smart Completion. Use Breadcrumbs to track your location inside the hierarchy of scopes. Gain insight into function calls thanks to parameter name hints. Find the context usages of a symbol or simply jump to it by typing its name. CLion will even make sure your code conforms to coding guidelines, including formatting, naming, and more.
## Code generation 
Generate tons of boilerplate code instantly. Override and implement functions with simple shortcuts. Generate constructors and destructors, getters and setters, and equality, relational, and stream output operators. Wrap a block of code with a statement, or generate a declaration from a usage. Create custom live templates to reuse typical code blocks across your code base to save time and maintain a consistent style.
## Safe refactoring 
Rename symbols; inline a function, variable, or macro; move members through the hierarchy; change function signatures; and extract functions, variables, parameters, or a typedef. Whichever automated refactoring you use, rest assured CLion will safely propagate the appropriate changes throughout your code.
## Quick Documentation 
Inspect the code under the caret to learn just about anything: function signature details, review comments, preview Doxygen-style documentation, check out the inferred type for symbols lacking explicit types, and even see properly formatted final macro replacements.
# References
【1】百度百科-VI(Unix及Linux系统下标准的编辑器)：https://baike.baidu.com/item/Vi/8987313#viewPageContent
【2】百度百科-emacs：https://baike.baidu.com/item/emacs
【3】王新旺,刘瑞静,蒋义然.Linux下文本编辑利器Emacs简介与安装过程[J].科技视界,2012(12):151+189.
【4】百度百科-VS code：https://baike.baidu.com/item/visual%20studio%20code/17514281?fr=aladdin
【5】Clion官网：https://www.jetbrains.com/clion/features/
