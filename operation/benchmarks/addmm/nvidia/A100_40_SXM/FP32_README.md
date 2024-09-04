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

https://github.com/FlagOpen/FlagGems. Commit ID: 3c10679326b32ea5f037db50cc397d41c0ff1934

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | True    | 18.4TFLOPS       | 18.39TFLOPS        | 94.34% | 94.3% |
| nativetorch | True    | 18.77TFLOPS      | 18.73TFLOPS      | 96.26%      | 96.07%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- |
| flaggems | 7473.76us       | 7477.25us        | 133.8op/s | 133.74op/s | 21083149.32us | 7553.75us |
| nativetorch | 7324.84us       | 7339.01us        | 136.52op/s | 136.26op/s | 84724.97us | 7346.76us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1725.75W | 1794.0W | 131.9W   | /     | 360.9W       | 366.0W      | 2.26W        | 400W  |
| flaggems监控结果 | 1706.25W | 1794.0W | 153.23W   | /     | 355.72W       | 360.0W      | 3.04W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.759%    | 1.094%   | 63.27°C       | 2.534%        |
| flaggems监控结果 | 0.746%    | 1.091%   | 62.83°C       | 2.534%        |