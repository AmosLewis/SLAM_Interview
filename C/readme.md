# C review note

### [***linux命令行编译运行方式***]
```
新建个test.cpp文件: touch  test.cpp
编译: gcc -o test test.cpp
运行: ./test
```

### 基本文件格式
```
#include "stdio.h"
int main()
{
    int a = 10;
    printf("the file format: %d\n",a);
    return 0;
}
```
### [***知识点***]
- 1.1 数据类型
  - 1.1.1 数据类型的概念
  
  - 1.1.2 数据类型的本质： [**固定内存大小的别名**]。
  
       - 作用： compiler预先算分配的内存空间大小, 但并没有开始分配空间，只有variable 创建了，才分配

       ```
       int a = 10
       int  告诉 compiler要分配4字节内存，看到 a 才开始正在分配分配
       ```
       
       

###  [***常见错误类型***]
#### 
