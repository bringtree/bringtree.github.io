个人简介

- 姓名: 黄培松
- 性别: 男
- github: [bringtree的github / 记录了平时遇到的一些问题的博客](https://github.com/bringtree/question_embedding/issues)
- 研究方向：人机对话
- 常用编程语言: py/js/cpp
- 邮箱: bringtree@qq.com
- 电话: 13433835659

学习/工作情况

- 2019.3 - 现在: 北京网易有道-语音实习生 (语音0基础,学习中)
- 2018.3 - 现在: SIGSDS实验室 (研究任务型对话系统)
- 2018.11 - 2019.3: CVTE中央研究院-nlp实习生 (研究检索型问答型对话系统)
- 2016.9 - 2020.7: 华南农业大学-本科生(计算机科学与技术)
- 2017.3 - 2017.10: 红满堂工作室-web开发

比赛经历

- 擅长领域： 短文本分类(意图|领域|新闻标题分类), 词向量后修正(同义反义问题,一词多义问题)

比赛经历

- 2018.5-2018.7中文人机对话技术评测用户意图领域分类比赛(排名:4/80).属于短句分类.由于测试集和训练集来自不同数据分布.所以主要是在词向量做了一些特征的补充.
- 2018.4-2018.5 NLPCC 2018 共享任务4子任务2意图识别(排名:4/195)(前三是搜狗,北京大学,CVTE.).由于数据集的标签很多会依赖到上文的句子,所以最后提交的模型是HierarchicalAttentionNetwork.

项目经历
- 2019.2-2019.3: 在CVTE中央研究院 使用 srcapy-redis 爬取百度知道相似问答对。
- 2018.12-2019.2: 在CVTE中央研究院 优化完线上问答机器人(微信公众号:希沃学院)的性能(主要是:用户反馈的解决率).主要是在做检索式的问答匹配.目前已将模型的top3从0.46提升到 0.76.
- 2018.11-2018.12: 在CVTE中央研究院 根据文本描述(内容是描述工作计划, 标签是(合格/不合格),)做二分类任务, 将文本的fn(即合格被误判成不合格) 降低到符合上线的要求. 减轻了人事部门的被投诉的次数(因为如果合格误判成不合格 会被投诉). 主要做法是:设置分类的阀值,修改最后一层softmax的改为
<img src="http://latex.codecogs.com/gif.latex?y_{i} = softmax(x-u_{i} , u_{i}) " />,其中x是上一层的输入,
<img src="http://latex.codecogs.com/gif.latex?u_{i}" />是全连接对应类别的向量.

- 2018.7-2018.11:提出另⼀种将主题模型(btm)和神经⽹络结合的方式来提高分类指标的方式(被拒,准备 改投CIKM)。期间编写了一个可视化attention的页⾯,方便样例分析.
- 2018.4-2018.6 基于可靠词汇语义约束的词语向量表达修正研究(论文第三作者，将第一作者的想法转换为代码实现，论文被CCL录用(CCL-18-066)。) 主要思路:是借助外在的词典来解决词向量同义词和反义词在维度上比较相似的问题.
(期间曾将估计计算量>1个月的代码优化到<1天):1.使用pyflame分析耗时长的地方,优化做缓存;2.将代码改为多进程;3.将代码的余弦计算改成可以用numpy大批量计算;4另外为做分析时能够随机调用词向量出来查看,利用grpc写了快速取词向量出来的脚本(将每次需要查看个词向量都需要预加载好几分钟的时间压缩的几秒).
- 2017.3-2017.9: 期间在做web开发.使用Koa+Vue开发学校团委的实时投票系统(背景:因为需要现场投票表决,参与投票人数很多，需要大量志愿者反复确认计票)和重构一个angular编写的森林防火的web应用.
