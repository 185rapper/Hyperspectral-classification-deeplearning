# Hyperspectral classification deeplearning
 使用深度学习方法实现小样本条件下的高光谱图像分类  
 author:lrybbs
## 简要说明  
> Q: 这个代码可以用来做什么水平的高光谱分类任务？  
A: 我写这个代码是为了完成我的本科毕设，我在本科期间几乎可以说从未接触过高光谱分类的内容，因此这个代码是我根据已有的论文的开源代码分析整理后重写的，功能比较粗浅，模型比较简单，唯一优点可能是我在我自己一开始也没搞懂的地方都写了注释。**适合第一次接触高光谱分类任务的本科生、以及没有高光谱分类工作经验的研究生入门用。** 不适合已经在高光谱领域已经有深入了解，需要更多功能的本科生（研究生）使用。

>Q: 这个代码的小样本从何体现？  
A: 其实没有太多体现，我参考的原论文虽然起名带有"few-shot"，但是实际上他的工作也和现在常见的小样本工作有所区别，没有那种1shot、5shot之类的那种小样本微调的操作存在，我写这个代码的时候对于小样本这个概念还处于一个似懂非懂的状态，所以这个代码的小样本就真的只是 **“使用的样本量比较少”** 了，如果对高光谱分类任务的基本知识已经很明了，需要做更深层次的小样本工作，可以再找找其他工作。

>Q: 为什么注释不用英文？  
A: 这并非一篇英文论文的附属代码，所以我干脆就拿中文写注释了，也方便大家看。说实话我当时读了很多遥感相关的论文，大部分都是中国人写的，我都一度怀疑这玩意是不是都是中国人在发。

>Q: 代码怎么运行？  
A: 理论上来说直接运行demo.py即可，这个代码是基于pytorch框架的，没有用到什么特别冷门的库，要是报错说有什么模块没找到的话pip install一下即可。至于添加自定义的网络结构也是可行的，可以参考hyper_net.py中已有的网络写法进行添加。支持的数据格式是npy格式的，其他格式的高光谱数据都可以用很简单的方法转存为npy格式 **（用专用的库读入，然后转成ndarray再np.save()）**，再使用本代码。

>Q: 还会更新吗？  
A: 我自己应该不会更新这个了，因为读研之后我的方向转成信号分类相关的工作了，对遥感工作的接触越来越少，实在抱歉。