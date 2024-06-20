# DLproject
2024Spring Deep Learning Group Project

随着深度学习技术的发展，图像描述（Image Caption）任务在计算机视觉与自然语言处理交叉领域受到了广泛关注。本报告旨在改进和微调现有的“看图说话”（Image Caption）方法，通过优化Encoder-Decoder架构，引入注意力机制与预训练模型，提升模型在复杂图像语境中的表现能力与泛化能力。

本报告回顾了图像描述任务的研究历程，包括基于模板匹配的方法、基于检索的方法以及近年来流行的Encoder-Decoder框架。在此基础上，本报告的Baseline Model采用卷积神经网络（CNN）和循环神经网络（RNN）组成的Encoder-Decoder框架，通过随机梯度下降（SGD）进行训练，并通过束搜索（Beam Search）等技术进行推理。然而，该模型在处理复杂图像时存在局限性，无法充分关注图像的局部特征。

为了解决这一问题，本报告尝试了基于Transformer的模型，通过缩放点积注意力机制使模型能够选择性关注输入的内容。进一步地，本文使用了Spatial and Channel-wise Attention Transformer（SCA Transformer），在视觉空间中结合了空间和通道维度的注意力，从而更加充分地学习图像特征。

此外，本报告还探讨了预训练模型在图像描述任务中的应用。通过利用在大规模数据集上预训练的CLIP与GPT2模型，小组构建了一个高效的图像描述生成系统。该系统利用CLIP的图像编码器提取图像特征，并通过GPT2作为文本生成器，实现了高质量的图像描述生成。

在实验部分，本报告在Flickr8k和Flickr30k数据集上对提出的模型进行了评估。实验结果表明，与Baseline Model相比，基于Transformer的模型和预训练模型在BLEU、ROUGE、METEOR和CIDEr等评价指标上均有显著提升。特别是在引入SCA模块后，模型在描述主题上的准确性得到了进一步提高。

综上所述，本报告通过改进和微调现有的Image Caption方法，提出了一系列有效的模型结构，并在实验中取得了显著的性能提升
![image](https://github.com/stonewang00/DLproject/assets/84163106/4571b237-b1de-4fbe-9205-e1441667d41a)
