# 欢迎参加NUDT超算招新挑战

很高兴您能够参加这个活动，本仓库作为模板仓库，您git clone下来即可。
我们会给您提供访问相应硬件的入口，请您发送您的学号、姓名以及单位到huangxihan@nudt.edu.cn，通过审核后将会给您提供相应账号密码。

本次挑战硬件配置（登录节点与评测节点环境保持一致）：
40GB A100 * 2
13th Gen Intel(R) Core(TM) i7-13650HX

我们提供测试环境给您，供您分析瓶颈及代码测试。
由于硬件资源有限，评测机暂时不支持并发测试，如果参加者过多，将会考虑扩增节点。

希望您能取得好成绩!

## CPU
测试环境编译：
g++ ./CPU_benchmark/cpu_benchmark.cpp cpu.cpp -I CPU_benchmark

提交评测机：
./client username passwd
随后会要求您输入评测文件，您输入cpu.cpp即可，也就是说您关于cpu版本所有的代码改动应该在cpu.cpp中，并且不应该修改文件名。

## GPU
测试环境编译：
nvcc GPU_benchmark/gpu_benchmark.cu gpu.cu -I ./GPU_benchmark -lcublas

提交评测机：
./client username passwd
随后会要求您输入评测文件，您输入gpu.cu即可，也就是说您关于gpu版本所有的代码改动应该在gpu.cu中，并且不应该修改文件名。

## 结果提交
此步骤，在您成功提交评测机后进行。
您将本仓库push即可
注意，请不要修改result中的任何内容，您根本不需要关心这个文件夹；您可以通过访问test文件夹来查看评测结果。

## 技术支持
本项目由计算机学院天河超算俱乐部提供技术支持，俱乐部还将举行一系列HPC入门讲座活动，期待您的参加！
如有任何疑问请发送邮件到huangxihan@nudt.edu.cn。