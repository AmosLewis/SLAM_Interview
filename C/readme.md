# C review note

### [***linux terminal compile and run***]
```
new a firl called test.cpp: touch  test.cpp
compile: gcc -o test test.cpp
Run: ./test
```

### C file format
```
#include "stdio.h"
int main()
{
    int a = 10;
    printf("the file format: %d\n",a);
    return 0;
}
```
### [***Knowledge Note***]
- 1.1 Datatype

	- 1.1.1 Classification of data type
	
		- simple: basic type(int,float/double, char, void), user-define-type/enum
	
		- struct:array[], struct, union, class
		
		- pointer: *

	- 1.1.2 Essence of data type： [**alias of fixed space of memory**]

		- Function： **Compiler** precalculate space of memory to be alloc, but it has not alloc. Only when the **variable** be created will the memory be alloc.

		```
		int a = 10
		"int"  tell Compiler to alloc 4 byte memory. When compile see "a", it will alloc. 
		```

	- 1.1.3 Size of data type

		- sizeof is operator，the same as (+ — * /), it is not a function.  Size will be return after compile.


		```
		// note the %zu, should not be %d, or it will return e1;
		printf("sizeof(a): %zu \n", sizeof(a))
		```

	- 1.1.4 Rename of datatype

	```
        // rename for struct
        typedef struct People
        {
	        char name[64];
	        int age;
        } people_t;
        // rename for unsigned int
        typedef unsigned int u32;
	```

	- 1.1.5 Void(Data Encapsulating: "nothing is impossible" type)

		- void* as left value, can point to any type of data

		```
		void* memcpy( void* dest, const void* src, size_t len );
		void* memset( void* buffer, int c, size_t num );
		void* malloc (size_t size);
		```
		
		- void* as right value, must be casted to other type of point, because ***C define only the same type of pointers can be allowed to assign with each other***.
		```
		char* p2 = (char*)malloc(sizeof(char)*20)
		```
		
		- void in function **pramater** and **return value**, means nothing.
		```
		int function(void)
		{
			return 1;
		}
		void function1(void)
		{
			return;
		}
		```
		
		- No void type variable
		
			C does not define the size of memory for void.

- 1.2 Variable
	- 1.2.1 Definition of Variable
	
		- Memory that can be read and write.
		
		- Alia of a continuous size of memory.

###  [***Common Error & Solution***]
[e1] ‘%d’ expects argument of type ‘int’, but argument 2 has type ‘long unsigned int’

[s1] 1.1.3  %d -> %zu

[stackflow-d-expects-argument-of-type-int-but-argument-2-has-type-long-unsigned-int](https://stackoverflow.com/questions/21128092/d-expects-argument-of-type-int-but-argument-2-has-type-long-unsigned-int)
