# 2018 “达观杯”文本智能处理挑战赛

[竞赛地址](http://www.dcjingsai.com/common/cmpt/%E2%80%9C%E8%BE%BE%E8%A7%82%E6%9D%AF%E2%80%9D%E6%96%87%E6%9C%AC%E6%99%BA%E8%83%BD%E5%A4%84%E7%90%86%E6%8C%91%E6%88%98%E8%B5%9B_%E7%AB%9E%E8%B5%9B%E4%BF%A1%E6%81%AF.html) 

baseline 参考 [baseline2.0：带你进前十](http://www.dcjingsai.com/common/bbs/topicDetails.html?tid=1522)， [tfidf+lr lb：0.77256](http://www.dcjingsai.com/common/bbs/topicDetails.html?tid=1479)

我这份 baseline 在上述两个开源的基础上主要对特征进行了选择，使用卡方检验、逆文档频率 idf，以及用带 L1 正则的基于模型的特征选择；另外除了提取 tfidf 特征之外还加入了词频计数特征。特征选择之后线下 cv 相较不选择提升了一个点左右，甚至可以达到 0.80，但是线上成绩没有提高，只有 0.77xxx，原因可能在于训练集和测试集分布不太一致，毕竟测试集中好像有几万个词没在训练集中出现过。

代码运行时间较长，不建议直接运行，可以在其他训练集测试集数据分布类似的数据集上进行尝试。

# 2018CCF 景区口碑评价预测竞赛Baseline

使用fasttext快速搭建文本分类模型，已录制视频讲解，[视频地址](https://www.bilibili.com/video/av19505310/)