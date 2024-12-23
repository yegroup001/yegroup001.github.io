# 香橙派 Zero 3

## 硬件配置

| 硬件 | 型号 | 备注 |
| ---- | ---- | ---- |
| CPU | Allwinner H618，4 核 Cortex-A53 @1.512GHz |  |
| 内存 | 1GB LPDDR4 1584MT/s, 32bit |  |
| 存储 | 32GB TF 卡 | 只能工作在 SDR50 模式 |
| 网络接口 | 1x RJ-45 |  |

## 超频

在给到的 Linux 镜像中，CPU 的 oop_table 设定在了 1.1V, 1.512GHz，而默认的 1.1V 的电压下，超频到 1516MHz 仍然可以正常使用，但是超到 1532MHz 就会直接 kernel panic（这是出厂即灰烬啊），故只能选择加压。查阅全志 H618 的 datasheet, 发现 soc 的推荐电压是 1.1V, 安全电压是 1.3V，故选择加压到 1.2V。