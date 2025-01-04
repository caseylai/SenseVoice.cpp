# SenseVoice.cpp

本项目fork自lovemefan的[SenseVoice.cpp](https://github.com/lovemefan/SenseVoice.cpp)，感谢原作者的贡献。

本项目用于构建个人语音项目的ASR后端，采用CPU实现非高并发情况下的ASR，节省GPU和API费用。

## 修改点

- 增加了全局的日志等级，避免输出太多日志
- 在state中为result_all增加了ASR结果保存，便于程序处理
