# idea

关于 voice conversion(VC) 的一些思考：

- ASR+TTS效果好但是不能实时？合并模型，模型蒸馏

- 特征解耦方法？表示学习，特征解耦

- 不能只有解耦需要配套的耦合方法？多功能的网络，encoder：两路输出，一路说话人信息，一路内容信息；decoder：两路输出与之前对应

- 结合自适应滤波器的思路？初始化一个帧级别的mask，一个判别器判断当前前n帧与目标说话人的相似程度，反向传播更新mask，效率？

- 效果评估？语音识别，说话人识别，语音质量，可用于设计 loss

- 信息解耦：必须知道解耦出来的对不对 + 相似性度量：不用知道是什么只用知道像不像

- 解耦的一个思路，针对提取说话人信息时，使用一个预训练的ASR和一个预训练的说话人识别，降低第二个loss的同时，提升第一个loss，反之同理

- 为什么 GAN 做 VC 效果不好？

- TTS, TTS + 风格迁移 => 分解出语音转换

- 研究目标：通用评估系统，实用、可定制、实时、轻量化 VC

- papers with code: https://paperswithcode.com/task/voice-conversion
- Awesome Voice Conversion : https://zhuanlan.zhihu.com/p/265149474
- 语音转换技术综述：https://zhuanlan.zhihu.com/p/89763124
- TTS(Speech Synthesis)的很多思路相似，可以学习vocoder等
- 一些 VC 大佬：
    1. https://www.zhihu.com/people/mai-zi-shou-liao-70
    2. https://www.zhihu.com/people/song-wen-le-88/asks
    3. 李宏毅

