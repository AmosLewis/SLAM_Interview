##### A1_(static_cast和dynamic_cast区别)
[Stackflow Link：regular-cast-vs-static-cast-vs-dynamic-cast](https://stackoverflow.com/questions/28002/regular-cast-vs-static-cast-vs-dynamic-cast) 

/Book/C++基础进阶的书里也有说明

- Same point: 

    - [1] [***Upcast***]("Up-cast" (derive->base class) is always valid )

    - [2] [***None Relevent Class***]( Report error during **compile** if cast two unrelevent class,如 char->int  在C里面就是可以的，C++里面就必须用, reinterpret_cast, 我们平时用的基本都是C风格的强制转换，就在变量前面加一个（要强转的类型）什么的。 )

- Different point: 

    - **static_cast** : 

        - [1] [***No runtime checks***] ( Used if you know that you refer to an object of a specific type, and thus a check would be unnecessary.)
  
        - [2] [***Downcast***]( Even cannot downcast, the static_cast won't give you error reprort during **compile**)
    
        - [3] [***No Polymorphic Argument Type***]( Class base don't need to have vitual function )
    
        - [4] [***Numerical Cast***]( Not only reference & pointer, but also numerical cast. )

    - **dynamic_cast** :

        - [1] [***Run Time Checks***] ( Used when you don't know what the dynamic type of the object. Returns a null pointer if cast fail.)

       - [2] [***No Downcast***]( Cannot be used base->derived class)

		- [3] [***Polymorphic Argument Type***] (多态 polymorphic means base 必须有 vitual function，这才是判断要不要用dynamic_cast的核心原因就看 base中有没有 vitual function, 参见[A3_(visual_function的作用)](cpp/A3_(visual_function的作用)) )

		- [4] [***Only Reference & Pointer***] (只能被用于 class 的reference and pointer)
