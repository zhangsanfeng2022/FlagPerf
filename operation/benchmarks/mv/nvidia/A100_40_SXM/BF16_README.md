# 参评AI芯片信息

* 厂商：Nvidia

* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1
* 单服务器内使用卡数: 1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID: 801377f03ba4649bc2d839ff34e38be66ee8a633

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | True    | 0.04TFLOPS       | 0.17TFLOPS        | 0.01% | 0.05% |
| nativetorch | True    | 0.15TFLOPS      | 0.17TFLOPS      | 0.05%      | 0.05%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | 
| flaggems | 48.26us       | 12.29us        | 20721.7op/s | 81380.21op/s | 19575635.47us | 68.19us |
| nativetorch | 14.39us       | 12.29us        | 69469.75op/s | 81380.21op/s | 162237.72us | 33.13us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1508.0W | 1560.0W | 73.54W   | /     | 157.94W       | 177.0W      | 20.48W        | 400W  |
| flaggems监控结果 | 1521.0W | 1560.0W | 39.0W   | /     | 167.0W       | 177.0W      | 13.13W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.84%    | 2.484%   | 37.56°C       | 3.461%        |
| flaggems监控结果 | 1.35%    | 2.484%   | 37.74°C       | 3.461%        |
