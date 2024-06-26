# 参评AI芯片信息

* 厂商：Nvidia


* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1


* 单服务器内使用卡数：1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID:982781081f5d62856064ae986e8927a31e96c235

# 评测结果

## 核心评测结果

| 评测项  | 平均相对误差(with FP64-CPU) | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | 0.00E+00    | 0.32TFLOPS       | 0.32TFLOPS        | 0.1% | 0.1% |
| nativetorch | 0.00E+00    | 0.32TFLOPS      | 0.32TFLOPS      | 0.1%      | 0.1%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 0.00E+00    | 6769.91us       | 6786.05us        | 147.71op/s | 147.36op/s | 262548.71us | 6835.66us |
| nativetorch | 0.00E+00    | 6778.26us       | 6795.26us        | 147.53op/s | 147.16op/s | 9427.55us | 6795.5us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1664.0W | 1716.0W | 36.77W   | /     | 255.12W       | 257.0W      | 3.16W        | 1664.0  |
| flaggems监控结果 | 1716.0W | 1716.0W | 0.0W   | /     | 293.74W       | 297.0W      | 3.46W        | 1716.0  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.525%    | 2.095%   | 49.42°C       | 26.483%        |
| flaggems监控结果 | 0.599%    | 2.093%   | 51.94°C       | 26.295%        |
