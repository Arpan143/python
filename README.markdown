# Python

可读性好，开发效率高是 Python 语言突出优点。

### 语法
    
    data structure
        
        - list
        - set
        - dict
    function
        
        - parameter
    generator and coroutines
        - 
    decorator
        decorator 装饰函数 func ， 指的是在 func 执行的前后，自动地执行其它逻辑的代码。
        
            - 如下 python 代码，相当于执行了 f = decorator(f) 语句。
                ```python
                # f = decorator(f)
                @decorator
                def f(*args, **kwargs):
                    ...
                ```
            - 函数 \_\_doc\_\_, \_\_anotations\_\_ 等等属性，需要保持（否则装饰前函数的 \_\_doc\_\_ 属性和装饰后的函数的 
            \_\_doc\_\_ 属性不一致）， python functools.wraps 函数能够保持函数的属性。 
            - 装饰普通函数 versus 装饰方法
                - method 属于 Function, method 的调用方式和普通函数不同。
                - 需要判断函数是不是以 method 的调用方式调用的。
                - 对于 method 可能需要不同的处理逻辑。
                
            - 所有 callable 的 ( 定义了 __call__ 方法 ) object 都可以作为 decorator
        
    metaclass
        - 
    namespace
        - 
    descriptor(access interception)
        - \_\_get\_\_
        - \_\_set\_\_
        
    manager context
        - 
    
    name mangling
        - 
    \_\_all\_\_ mechanism
    
    reflection
        - getattr
        - 
    
    multiple inherit

\_\_dict\_\_
dir
types    


### 代码规范
    
    参见 [pep8](https://pep8.org)。
       
### 测试
    
    python 单元测试常用的框架：
        - pytest（推荐使用） 
        - doctest 
        - nosetest 
        - unittest 
    
    python 支持 BDD 的开发模式，python 中支持 BDD 的框架有：
        - Behave
        - lettuce
    
    python 的构建工具：
        - [tox](https://tox.readthedocs.io/en/latest/)
        - [buildout](http://www.buildout.org/en/latest/)
    
    以上框架， Pycharm 都支持(提供了可视化的使用窗口，提供了工具分析展示构建结果)。 

### 性能调优
    
    python 中分析程序性能的框架有：
        - cProfile
        - yappi
        - VMprof
    
    这三个框架，都会产生 Statistics（统计每部分代码运行耗时） 和 Call Graph （统计函数相互之间的调用关系）。
    pycharm 支持上述框架（提供了可视化的使用界面），并提供工具分析 Profile 的结果（cProfile， yappi, VMprof 
    分别产生 .pstat，.yappi， .vmprof 文件）。
    

### 网络服务

    python 中构建网络服务的框架有:
        - django
        - flask
        - tornado
        - 其他的我没有用过
        
### 数据库

    python 中处理数据库最有名的框架是：
        - SQLAchemy

### 科学计算数据分析和机器学习

    python 中用于科学计算的工具有：
        - numpy
        - matplotlib
        - pandas
        - scipy
        - skilearn
        - tensorflow

### 构建工具

    python 中用于构建项目的工具有：
        - tox
        - buildout

### 文档

    python 常用的文档格式(docstring style)有两种：
        - restructure text
        - Epytext
        
### 日志
    python 日志模块：
        - logging( 非常类似 Java 中的 log4j )

### 配置文件
    常用的日志文件有 ini 格式和 yaml 格式

### 参考文献

- [Python Cookbook]()
- [pep8 code style guide](http://pep8.org)


***English translated***
# Python

Good readability and high development efficiency are outstanding advantages of the Python language.

### Syntax
    
    data structure
        
        -list
        -set
        -dict
    function
        
        -parameter
    generator and coroutines
        -
    decorator
        The decorator decoration function func refers to the code that automatically executes other logic before and after the execution of func.
        
            -The following python code is equivalent to executing f = decorator(f) statement.
                ```python
                # f = decorator(f)
                @decorator
                def f(*args, **kwargs):
                    ...
                ```
            -Functions \_\_doc\_\_, \_\_anotations\_\_ and other attributes need to be kept (otherwise the \_\_doc\_\_ attribute of the function before decoration and the attribute of the function after decoration
            \_\_doc\_\_ attributes are inconsistent), python functools.wraps function can maintain the attributes of the function.
            -Decorating ordinary functions versus decorating methods
                -Method belongs to Function, and the calling method of method is different from ordinary functions.
                -It is necessary to determine whether the function is called in the method of calling.
                -Different processing logic may be required for method.
                
            -All callable objects (with __call__ method defined) can be used as decorators
        
    metaclass
        -
    namespace
        -
    descriptor(access interception)
        -\_\_get\_\_
        -\_\_set\_\_
        
    manager context
        -
    
    name mangling
        -
    \_\_all\_\_ mechanism
    
    reflection
        -getattr
        -
    
    multiple inherit

\_\_dict\_\_
dir
types


### Code Specification
    
    See [pep8](https://pep8.org).
       
### Test
    
    Common frameworks for python unit testing:
        -pytest (recommended)
        -doctest
        -nosetest
        -unittest
    
    Python supports BDD development mode. The frameworks that support BDD in Python are:
        -Behave
        -lettuce
    
    Python build tools:
        -[tox](https://tox.readthedocs.io/en/latest/)
        -[buildout](http://www.buildout.org/en/latest/)
    
    The above frameworks are supported by Pycharm (a visual window is provided, and tools are provided to analyze and display the construction results).

### Performance Tuning
    
    Frameworks for analyzing program performance in python are:
        -cProfile
        -yappi
        -VMprof
    
    These three frameworks will generate Statistics (to count the running time of each part of the code) and Call Graph (to count the calling relationships between functions).
    pycharm supports the above framework (provides a visual user interface), and provides tools to analyze the results of the Profile (cProfile, yappi, VMprof
    Generate .pstat, .yappi, .vmprof files respectively).
    

### Internet service

    The frameworks for building network services in python are:
        -django
        -flask
        -tornado
        -I haven't used the others
        
### Database

    The most famous framework for processing databases in Python is:
        -SQLAchemy

### Scientific Computing Data Analysis and Machine Learning

    The tools used for scientific computing in python are:
        -numpy
        -matplotlib
        -pandas
        -scipy
        -skilearn
        -tensorflow

### Build tools

    The tools used to build projects in python are:
        -tox
        -buildout

### Documentation

    Python commonly used document format (docstring style) has two types:
        -restructure text
        -Epytext
        
### Log
    Python log module:
        -logging (very similar to log4j in Java)

### Configuration file
    Commonly used log files are ini format and yaml format

### references

-[Python Cookbook]()
-[pep8 code style guide](http://pep8.org)
