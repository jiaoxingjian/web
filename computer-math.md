# dou 数学 x 编程 x 物理 
## 初等数学
- 计算机作图
  - [知识汇总](https://github.com/orgs/youtechno/projects/5)
  - [平面几何中的平行]()
    - [x] 概念
    - [x] 判定
    - [x] 性质
    - [ ] 和函数的关系
  - [坐标系]()
    - [x] 平面坐标系
    - [x] 球面坐标系
  y=kx中的k决定了直线的防线，k相同，则平行（不重合前提下）
  作图说明
```
from sympy import *
init_printing()
x,y,z =symbols('x y z')
f = plot(x+5)
f
```
  ![](https://i.imgur.com/onKCUBT.png)
```
f2 = plot(2*x+10)
f2
```
![](https://i.imgur.com/nruF6zj.png)

## python解方程
- [x] [解二元一次方程组](https://blog.csdn.net/jacke121/article/details/78491225)
![](https://i.imgur.com/7UtMG5E.png)


```
from sympy import *
x = Symbol('x')
y = Symbol('y')
print(solve([3 * x + 5 * y - 19, 4 * x - 3 * y - 6],[x,y]))

```
- [ ] [解不等式官方doc](https://docs.sympy.org/latest/modules/solvers/inequalities.html)
- [ ] 例子
```
from sympy import sympify as S, Symbol
from sympy.abc import x, y
from sympy.solvers.inequalities import reduce_inequalities
Run code block in SymPy Live
reduce_inequalities(0 <= x + 3, [])

```
![](https://i.imgur.com/GLbmGJQ.png)

## numpy
线性方程组求解
求解线性方程组比较简单，只需要用到一个函数(scipy.linalg.solve)就可以了。比如我们要求以下方程的解，这是一个非齐次线性方程组：
3x_1 + x_2 - 2x_3 = 5
x_1 - x_2 + 4x_3 = -2
2x_1 + 3x_3 = 2.5
```
import numpy as np
from scipy.linalg import solve
a = np.array([[3, 1, -2], [1, -1, 4], [2, 0, 3]])
b = np.array([5, -2, 2.5])
x = solve(a, b)
print(x)
输出结果：

[0.5 4.5 0.5]
```

> 不等式
- [ ] [不等式](https://www.youtube.com/watch?v=J053g1TBb00)
> 数形结合思维
- [ ] [学而思 六年级 四大数学思想-数形结合在应用、行程问题中的应用知识点](https://www.youtube.com/watch?v=lZbZPdGzqxw)
- [ ] [初中生最怕考的题目！数形结合到底难还是不难？](https://www.youtube.com/watch?v=sjenQ9P4mxE)
- [ ] [数形结合典型题](https://www.youtube.com/watch?v=jJqQOxS3XQI)
- [ ] [数形结合思想-基本尺规作图](https://www.youtube.com/watch?v=-zx_nk0hjGQ&t=94s)


### dou 初等数学   
- [algebra](https://docs.sympy.org/latest/tutorial/simplification.html)
- simplify
  - [x] [expand](https://docs.sympy.org/latest/tutorial/simplification.html#expand)
  - [x] [factor](https://docs.sympy.org/latest/tutorial/simplification.html#factor)
  - [x] [collect](https://docs.sympy.org/latest/tutorial/simplification.html#collect)
  - [x] [cancel](https://docs.sympy.org/latest/tutorial/simplification.html#cancel)
  - [x] [apart](https://docs.sympy.org/latest/tutorial/simplification.html#apart)
  



## 数学分析
- [ ] [caculator ](https://www.symbolab.com/)

- [ ] [Algodoo Physics Simulation Tutorial ](https://www.youtube.com/watch?v=fMs4R-HQeH0)

- [ ] [Pendulum Motion in PYTHON](https://www.youtube.com/watch?v=ENNyltVTJaE&t=441s)

- [ ] [Derivatives In PYTHON (Symbolic AND Numeric)](https://www.youtube.com/watch?v=DeeoiE22bZ8&t=145s)

- [ ] [Fox-Rabbit Chase Problem [Solution & Math Proof]](https://gauravtiwari.org/famous-fox-rabbit-chase-problems-3/)

- [ ] [fox rabbit ](https://personalpages.manchester.ac.uk/staff/yanghong.huang/teaching/MATH36032/diffeq2.pdf)

  ![image-20230610164152794](.\Img\image-20230610164152794.png)

- [ ] [ode in physics](https://www.sharetechnote.com/html/DE_Modeling_Example_PreyPredator.html)

## matrix

  矩阵和微积分/概率 结合起来，得到了非常强大的应用。



 - [ ] [2d数学](https://www.youtube.com/watch?v=DhC_I9K-ZL4&list=PLXH05kw-i_5KM8eOHFxwubSi4F4pypz7Q)

 - [ ] [3d数学](https://www.youtube.com/watch?v=IK71fTxZpgk&t=26s)

- [ ] [3d建模软件meshroom](https://www.youtube.com/watch?v=R0PDCp0QF1o)

- [ ] [3d工业](https://www.youtube.com/results?search_query=%E5%BE%B7%E5%9B%BD%E6%9C%BA%E5%BA%8A)

- [ ] [Let's code 3D Engine in Python from Scratch](https://www.youtube.com/watch?v=M_Hx0g5vFko)
  
  - [source code](https://github.com/StanislavPetrovV/Software_3D_engine)
  
- [ ] [Adjacency Matrices - Two Step Connections](https://www.youtube.com/watch?v=bksS0_4mOv8&pp=ygUfY29tcHV0ZXIgYWxnb3JpdGhtIG1hcmtvdiBjaGFpbg%3D%3D)

- [ ] [youtube resource ](https://www.youtube.com/results?search_query=leetcode+matrix)

- [ ] [Creating a DOOM (Wolfenstein) - style 3D Game in Python](https://www.youtube.com/watch?v=ECqUrT7IdqQ&t=1846s)

  

## 概率

- [Gentle Introduction to Modeling with Matrices and Vectors: A Probabilistic Weather Model](https://www.youtube.com/watch?v=K-8F_zDMDUI&list=PLMrJAkhIeNNTYaOnVI3QpH7jgULnAmvPA&index=3)

- [Markov Chains Clearly Explained! Part - 1](https://www.youtube.com/watch?v=i3AkTO9HLXo)

- [A Random Walk & Monte Carlo Simulation || Python Tutorial ](https://www.youtube.com/watch?v=BfS2H1y6tzQ&t=316s)

- [【数之道 30】隐马尔可夫模型在NLP中的应用 Hidden Markov Model in Natural]https://www.youtube.com/watch?v=SAd24in2CDE)

  

- [python counter](https://www.google.com.hk/search?q=python+Counter&oq=python+Counter&aqs=chrome..69i57j69i59l3.3578j0j4&sourceid=chrome&ie=UTF-8)
- [python jieba]()



- ai



## data science



## caculus

- [ ] [Take Integrals 300X Faster in Python With GPU (DON'T Use SciPy)]()



- [ ] [Take Integrals 300X Faster in Python With GPU (DON'T Use SciPy)]()

- [ ] [Take Integrals 300X Faster in Python With GPU (DON'T Use SciPy)]()

- [ ] [Take Integrals 300X Faster in Python With GPU (DON'T Use SciPy)](https://www.youtube.com/watch?v=GOiTF11umMo)
- [ ] [pytorch tutorial ](https://www.youtube.com/watch?v=v43SlgBcZ5Y&list=PLkdGijFCNuVk9fO1IMfdV1Igob0FUHhkB&pp=iAQB)



## fourier transform





## signal process / z transform





## audio && video

- - [x] )
    -



### 图论



### 金融

- [ ] https://www.youtube.com/watch?v=4MiAZ-5_WnU
- [ ] https://www.youtube.com/watch?v=iSQipTxiqH0&list=PLwEF1U7kKqZbNYCFQEmFgkfSbTKuG5Q0g&index=1&t=5s