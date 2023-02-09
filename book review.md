如何科学地提问 观后感
开篇我想先说明文章中提到的四个缩写
RTFM: Read the Fucking Manual
STFW: Search the Fucking Web
RTFSC: Read the Fucking Source Code
我们的项目中称这是“大佬三连”。这不仅应该是大佬的专属，从另一个角度说我们又何尝不是曾说过或者至少想说过这些话的人呢。曾经我们也会被一些弱智问题问的很烦，但遗憾的是我问大多数都没有记住当时自己对别人的那种无奈感，知道某天真正的被人提出来才去思考。

关于RTFSC
我之前在大一想做机器学习的时候写过一段 Linear neural network 的代码并在训练中出了很大的问题。当时是想做一个Linear Regression的任务。虽然是个很简单的任务，但里面的数学推导我至今觉得并不很简单，需要用到线性代数和微分一类的推导
for month in range(12):
    for day in range(20):
        x[month*18:month*18+18,day*24:day*24+24] = data[month*20*18+day*18:month*18*20+day*18+18,:]

for month in range(12):
    for group in range(471):
        y[month*471+group] = x[month*18+9,group+9]

for month in range(12):
    for group in range(471):
        for i in range(9):
            x_list[month*471+group,i] = np.sum(x[month*18:month*18+18,group+i])

gradient_w = 2 * np.dot(x_list.T , y_train-y)
gradient_b = 2 * np.sum(y_train-y)
w = w - learning_rate * gradient_w
bias = bias - learning_rate * gradient_b
大概就是这几行代码，错误的地方只是里面哪个+-号写反了，但我当时问问题的时候给师哥发的是一整段代码，包括前面数据处理的部分。其实当时随着数据集下载下来的资料里还有吴恩达老师的例程，也许这个错误在我仔细看完源码后就查出来了。但我当时只是看了一眼发现里面的变量命名和我的不大一样就懒得看了，实在是懒得无可救药。但还有值得庆幸的部分就是也许我在那时就有独立思考尝试自己解决问题的能力。因为当时我只是看了一讲关于Linear Regression 的原理的视频就开始着手于算法的代码实现，也算是解决的很多困难才来到了最后的不调库实现自己的简单卷积神经网络。

关于RTFM和STFW
在学单片机的时候，不论51还是32相信大家都是从正点原子或者野火又或者原版的开发板用户手册开始的。我觉得这就是一个最好的例子。在这方面我自认为自己做的一直都不错，手册加上网络基本能解决一切的问题了。这也为我后来做FPGA一些简单的模块调用提供了很多的经验。但很可惜由于疫情和手术的缘故，可能没有机会在电子设计大赛正赛上展示了。
总之，以上就是我关于《如何科学的提问》想到的自己的经历了，在读完这两篇文章后我可能也会有些畏惧提问，怕自己提出一些很智障的问题被嘲笑。但只要确保自己完成了分内的事情，就不必担心是否会引来嘲笑，也许就是这样的守则才能维持一个良好的社区环境。
再写完这些后我突然想起来之前困扰过自己很久的关于D触发器和锁存器的问题，这次一定要全部弄清楚。
就先这样吧，也许以后会有更有趣的故事收录在这个文档里……
