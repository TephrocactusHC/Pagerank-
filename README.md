# Pagerank-
仅有一个readme，给大家提供一些参考
# PageRank
NKU-BD课程期中作业<br>
no_networkx_pagerank.py是完全自己实现的，但由于直接使用了numpy的矩阵乘法，不符合要求。最后提交的其他的code都参考了往届的代码并做了优化。<br>
主要实现了basic_pagerank和block_stripe update algorithm。<br>
**实际上，如果考虑到block_stripe的背景，即内存连r都存储不下的话，那么程序本身会非常复杂：<br>**
**首先，对数据的读取就应该分块读取，而不是直接open()或者loadtxt()，然后一次次的更新存储在硬盘上的M和r_old，这会相当慢而且繁琐。最后是更新r_new，计算过程本身并不困难，手动实现一个矩阵乘法然后不停I/O数据即可。但是在最后输出前100个节点的时候，因为r存不下，理论上需要应用外排序算法，而不是直接sort()。所以，总体来说我们目前所写的程序不可能应用到实际环境中，仅仅是对算法的简单模拟。<br>**

根据我看过的往届的代码，还没有人能够完美实现上述的block_stripe的每一个小细节，不过在22spring的课程中，因为不停有人提问使得老师把要求说得很细，应该是有人比较完整的实现了的，后面的同学可以问问。当然，这门课的助教认为不同的人对“时间换空间”有不同的理解，同学们进行各种相关的探索即可，不作为主要得分失分的依据。<br>
<br>
不得不佩服networkx和scipy这两个库，实在是过于强大了。相信手动实现大数据相关内容和图算法之后，会深有体会。<br>
## 下面附上一些我参考的往届学长学姐的代码链接，很多内容值得我们学习，希望对大家有所帮助。如果你要借鉴，请给他们Star！<br>
### 当然，如果我的程序和README.md对你有帮助，也请给我Star，多谢!

#### PYTHON版本
1.[SYD版本，比较符合课上对block_stripe的描述，实现了Matrix和R的分块。我的手动实现矩阵乘法借鉴了他的代码。](https://github.com/Emanual20/2021NKU_MassiveData_hw1) <br>
2.[不知名往届版本，我的分块思路部分借鉴了他的想法。](https://github.com/NKU-EnochYang/PageRank-with-Python/blob/master/page_rank) <br>
3.[ZXY版本，上古战神之一，代码较长，偏工程，可能是为了解决打包成exe时遇到的问题，不然这么长很奇怪。](https://github.com/kypomon/NKU_big-data_PAGERANK) <br>
4.[不知名往届版本，代码较短，不过有些细节不是手动实现。](https://github.com/Epiphqny/Pagerank) <br>
5.[不知名往届版本，我的数据加载主要借鉴他的想法。但是他对block_stripe的理解与课程要求不一致](https://github.com/lifengheng/pagerank) <br>
6.[外校的版本应该是](https://github.com/wymli/PageRank) <br>
7.[不知名往届版本，分块更新可供参考](https://github.com/cdasl/big-data_pagerank)<br>
8.[不知名往届版本，分块更新可供参考](https://github.com/yzy-source/PageRank)<br>
9.[不知名往届版本，少数实现了R的分条的，即stripe，有参考价值](https://github.com/gitdxj/teleport-pagerank)<br>
10.[不知名往届版本，有实验报告和讲解，可供参考](https://github.com/Joshua-li-yi/PageRank)<br>

#### C++版本
1.[不知名往届版本](https://github.com/New-Future/PageRank) <br>
2.[LSY版本](https://github.com/NKU-Yang/PageRank)<br>

#### python和C++均有，并实现并行化
1.[不知名往届版本，上古战神之一，实现了并行化](https://github.com/seasonyao/pagerank)<br>
2.[上面这个上古战神的csdn，如果你没听课的话，看他这个也可以](https://blog.csdn.net/codes_first/article/details/81090142)<br>

***ps:如果这学期选了算法导论、并行程序设计、大数据计算及应用，那么你可以用pagerank交三个课的大作业。(手动狗头)***

#### 本章节电子版课件，可以下载来参考。当然了老师自己也会发课件
[可能是斯坦福的，和老师的课件一样](https://xuhappy.github.io/courses/BigData/lecture/pagerank.pdf)
<br>
#### 本门课程中文版教材的图片，在图书馆七楼可以借阅这本书
![image](https://github.com/TephrocactusHC/PageRank/blob/main/book.jpg)

