### 第一章

#### 1.1 没啥记录的 第一章就是tour

##### 1.1.1 class部分的知识点

------------------------

_CPP_ 确实很难学，就__C__ 基础部分简单一点，但是__CPP__ 分两块重点类和模板。

类重点就是类的单个组成，包括__Detor__ 和__Ctor__ 这两个部分，**constructor** 部分又分了集中不同的*COPY* 初始化Cotr之类的。这就是单个*class* 的组成部分。当单个*class*说完了就可以把他们联系起来，比如多个组合继承之类的的关系。多个***class***之间的相互继承，初始化的表现和销毁的表现应该如何设计。这些东西是***inheritance***考虑的问题。还有支持***OOP***的设计，比如**继承，多态，虚函数** [^Inheritance Mophorise Virtrue]这些都是如何表现的。

***CLASS***之间又是如何互助或者串门的。这引入了*friend*关键词来达成这个目标。

既然是扩展了*C* 的集合，管理内存肯定是重头戏，把沉重的内存管理负担通过一些技术手段减轻就显得比较重要。在***CPP*** 中为了让内存管理容易变得容易，可以使用*Smart Pointer* 来管理动态内存。<u>尽量在代码中使用*Smart Pointer* 来管理动态内存</u>。

 

1. ***Code Viewer*** 深入___class___的各个细节 然后说明其作用

    ```c++
class Base{
    public:
    Base() = default; //默认
    Base(Base& ba);
    Base(Base&& ba);
    Base& operator=(Base& a, Base& b);
    
        
    protect:
const int get_value();
    
    private:
    const int pp;
    static int pp;
    double* pd;
    
    
    ~Base() = default; 
    };
    ```
    
2. ***KEY WORD*** 解释语义

    ***class***

    ***public***

    ***private***

    ***virtrue***

    ***override***

    ***const***

    ***static***

    ***friend***

    ***nonexcept***

    ***=default***

    ***=0***

    



```c
typedef struct _olist{
    ptrToNode head;
    function adding, deleting, access; // a type pointer to function
} olist;


// 当C需要继承的时候，如果按照常规的继承，只能嵌套多个struct，这中方法会带来沉重的命名负担，和过长的路径。
// 还好可以使用匿名struct来解决这个问题。

typedef struct _dlist{
    olist;     			  // 使用匿名结构 可以直接访问
    function repalcement; //添加一个函数操作list
} dlist;

```



##### 1.1.2 模板相关的知识

--------

模板是编译时多态，有些专有名词，模板特例化





##### 1.1.3 STL

---------

STL库是采用模板作为技术支持，具有组件，算法，容器，迭代器，仿函数

STL的核心库是算法和容器，中间的桥梁是iterator。 

