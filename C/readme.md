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
  - 1.1.2 数据类型的本质： 固定内存大小的别名。

###  [***常见错误类型***]
####
