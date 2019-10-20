---
marp: true
theme: uncover
paginate: true
author: fky
---

# Python tutorial

Python 不完全教程

<br />

*不完全的意思就是，对任何名词有问题，需要你自行搜索学习*

---

### 本篇不会涉及

- Python 的安装
- Python 的发展历史
- 手把手的、具体的代码（因为这是重复劳动，并且网上已经有大量优秀的例子）

<br />

*以上内容请自行 Google 学习*

---

### 本篇将主要涉及

- Python 与 C 的异同
- pip 是什么
- 列举在 CTF 中，常用的 Python 库
- Python 的学习方法
  - 学习资源推荐
- 其他的一些需要关注的问题

*以上内容不是目录呦*

--- 

### 关于 Python 入门推荐

- [廖雪峰的 Python 教程](https://www.liaoxuefeng.com/wiki/1016959663602400)
  - 如果是纯新手，可以先看前几章（比如看到`切片`）
  - 后面的内容需要有一定代码量才能理解
- [官方文档](https://docs.python.org/3/)
  - 正确的使用方式是通过搜索引擎进入到具体的内容中
- [A Byte of Python](http://www.swaroopch.com/notes/python/)
  - 一本开源的小书
  - 易懂，可以很快就看完

*以上内容都可以在网上找到，不需要任何实体读物*

---

### 关于 Python 进阶推荐

- [Python CookBook](https://python3-cookbook.readthedocs.io/zh_CN/latest/)
  - 开源
  - 大量 Edge Case
- [Real Python](https://realpython.com/)
  - 从简单的语法到复杂的最佳实践，这里都有
  - 作者还是很用心的

---

### 其他

- 好好使用搜索引擎！
- Stack Overflow
- GitHub
- GeakforGeak
- Redit

...

---

## 个人推荐的学习方式

#### 项目驱动学习
  
- 把 Python 当做一种工具而不是学习的目标本身，会让学习速度变得快很多
- 可以以 CTF / ACM / Web 开发 中的目标作为切入点
  - 能学到很多其他知识
  - 比如很多人会选择写爬虫来学习 Requests 库
    - 当然现在有 Requests-HTML 了（小声
- 写代码、看语法、看教程三者轮番进行

---

## Python 与 C

---

### 语法层次的异同

```Python
for i in range(15):
    if i in [3, 5, 6, 7, 9]
        print(f"I got {i}!")
```

```C
for(int i = 0; i< 15; ++i){
    if( i == 3 || i == 5 ){
        printf("%d", i);
    }
}
```


---

### 数据类型的异同

- 基本数据类型的存储方式
- Python 特有的字典、列表等
  - 在 C/C++ 中有哪些类似的数据结构
- Python 的动态类型
  - 比如 `[1, 'apple', ['sublist']]`
- Python 的鸭子类型
  - 函数传参不需要指定类型
  - 约等于多态

---

### 使用方式的异同

```Bash
vim test.c # 使用编辑器编辑代码
gcc test.c -o test.out # 预处理，编译，链接
./test.out # 执行
```

```Bash
vim test.py 
python test.py # 使用解释器直接执行
```

```Bash
python # 进入 Python 解释器的交互程序
```

---

### Wait But Why

编译型语言和解释型语言的区别
- `解释` v.s. `编译`
- GC
- `泛型` v.s. `弱类型`

---

## PIP

---

Python 的第三方库的集中存储仓库是 [PyPI](https://pypi.org/)。 PIP 作为包管理工具，负责从 PyPI 中拉取第三方库，并管理本地的依赖（可以理解为软件商店）。

*记得要配置源哦*

---

# Python 常用库

**如果你是入门者，以下内容只需走马观花即可**

---

### 网络

- [Requests](https://github.com/psf/requests) (或见[项目主页](https://requests.readthedocs.io))
- [socket](https://docs.python.org/3.7/library/socket.html)

---

### 爆破常用

- itertools
- [Multiprocess](https://docs.python.org/zh-cn/3/library/multiprocessing.html) 多进程


---

### 密码学

- gmpy2 数学运算
- PyCrypto 现代密码学的实现

---

### Pwn

- pwntools (似乎在3已经可用，但是大多数教程还是按照2来的)

---

# Python's Future

- Type Annotation
- Async
- Functional Programming
- ???

---

其实感觉写的时候有很多很多细节的地方可以写，但是想想真的很难梳理出一个清晰的思路；所以最后更多的是写出一些比较大的 Picture。Python 作为一种工具，可以作为大家真正入门的第一门语言（大雾）。

---

Talk is cheap, show me your code.
