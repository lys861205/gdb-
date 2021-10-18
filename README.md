# gdb常用命令
## 函数相关命令
* info functions 列出所有执行的函数
* info functions regex 查找匹配到的函数
* step（缩写s) 进入函数
* next（缩写n) 跳过函数
* finish（缩写f）退出正在执行的函数
* call或print 调用函数
* i frame 打印堆栈信息
* i registers 查看继存器
* bt 显示调用栈
* frame 选择栈帧
## 断点相关命令
* 命名空间设置断点
```
namespace {
void foo(){}
}

namespace Foo {
void bar(){}
}

匿名空间设置断点 b ::foo
有名空间设置断点 b Foo::bar
```
* 函数名称设置断点
```
void test(int a, int b)

b void test(int a, int b)
```
* 文件行设置断点
```
b File.cpp:10
```
