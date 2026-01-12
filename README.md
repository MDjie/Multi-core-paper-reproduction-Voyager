# 模拟平台模拟步骤


## 下载Traces:

在地址(https://utexas.box.com/s/2k54kp8zvrqdfaa8cdhfquvcxwh7yn85).  下载trace并解压为txt文件到 需要将473.astar-s0 训练trace下载到trace/train中


## 然后执行进行模拟
运行下面代码编译C++代码
```
./ml_prefetch_sim.py build
```
运行下面代码生成无预取器的基线结果
```
./ml_prefetch_sim.py run path_to_champsim_trace_here
```
path_to_champsim_trace_here 为测试trace的xz文件路径
运行下面代码将预取结果在模拟平台模拟运行

```
./ml_prefetch_sim.py run path_to_trace_here --prefetch path_to_prefetcher_file --no-base
```
path_to_trace_here 为测试trace的xz文件路径  path_to_prefetcher_file 为预取文件路径，目前Voyager，ISB，BO，STMS预取器生成的文件都在./predict下
最后的模拟结果保存在473.astar-s0.trace.gz-from_file.txt 中。

