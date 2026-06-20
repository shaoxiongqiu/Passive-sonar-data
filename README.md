# Self-Collected Passive Sonar Dataset

This repository provides a self-collected passive sonar dataset for research on **bearing‑only target tracking**, **signal denoising**, **filtering algorithm validation**, and **target motion analysis**. Researchers and practitioners are welcome to download, use, and exchange ideas.

---

## 📊 Field Definitions

| Field | Unit | Description |
|-------|------|-------------|
| `obs_x` | metre (m) | X‑coordinate of the observer (receiving platform) in the global frame |
| `obs_y` | metre (m) | Y‑coordinate of the observer in the global frame |
| `bearing_meas` | degree (°) | Noisy bearing measurement (clockwise from the global X‑axis) |
| `bearing_true` | degree (°) | True bearing (noise‑free, for performance evaluation) |
| `snr_meas` | decibel (dB) | Estimated signal‑to‑noise ratio of the measurement |
| `target_x` | metre (m) | True X‑coordinate of the target in the global frame |
| `target_y` | metre (m) | True Y‑coordinate of the target in the global frame |
| `bearing_body_meas` | degree (°) | Bearing measured in the body‑fixed frame (relative to the bow) |
| `time` | second (s) | Timestamp (starting from 1, increasing uniformly) |

> **Note**: Bearings are measured clockwise from north (or the positive X‑axis). A `bearing_true` value of 0 may indicate missing or invalid data; please filter accordingly for your application.

---

## 🎯 Intended Research Applications

- **Bearing‑Only Target Tracking**  
  Estimate the target trajectory using `bearing_meas` and observer positions `(obs_x, obs_y)`, and compare against the ground truth `(target_x, target_y)`.

- **Signal Denoising and Filtering**  
  Validate Kalman filters, particle filters, adaptive filters, and other denoising algorithms using both `bearing_meas` and `bearing_true`.

- **SNR Impact Analysis**  
  Analyse the statistical characteristics of bearing errors under different SNR levels via `snr_meas`.

- **Target Motion Model Identification**  
  Build constant‑velocity, constant‑acceleration, or manoeuvring models from the target position sequence.

---

## 📖 Citation

If you use this dataset in your research, please cite the following two papers:

```bibtex
@ARTICLE{QIU11418655,
  title={MPPI-DWIT: Robust Bearing-Only Target Tracking of Single AUV With Detection Sector Constraints}, 
  author={Qiu, Shaoxiong and Xu, Hongli and Wang, Junyi and Ru, Jingyu and Zhang, Wenrui and Wang, Jia},
  journal={IEEE Transactions on Automation Science and Engineering}, 
  year={2026},
  volume={23},
  number={},
  pages={6175-6189},
  doi={10.1109/TASE.2026.3669656}
}

@article{QIU2026123409,
  title = {Dynamic target tracking and pursuit for single AUV with bearing-only constrained sonar},
  author = {Shaoxiong Qiu and Hongli Xu and Jingyu Ru and Wenrui Zhang},
  journal = {Ocean Engineering},
  volume = {343},
  pages = {123409},
  year = {2026},
  issn = {0029-8018},
  doi = {https://doi.org/10.1016/j.oceaneng.2025.123409},
  url = {https://www.sciencedirect.com/science/article/pii/S0029801825030926}
}


# 自采被动声纳数据集（Passive Sonar Dataset）

本仓库提供一套自行采集的被动声纳实测数据集，适用于**方位角目标跟踪（Bearing‑Only Tracking）**、**信号降噪**、**滤波算法验证**以及**目标运动分析**等研究方向。欢迎学界同仁下载使用与交流探讨。

---

## 📊 字段定义

| 字段名 | 单位 | 描述 |
|--------|------|------|
| `obs_x` | 米（m） | 观测站（接收平台）的 X 坐标（全局坐标系） |
| `obs_y` | 米（m） | 观测站（接收平台）的 Y 坐标（全局坐标系） |
| `bearing_meas` | 度（°） | 含噪声的方位角测量值（相对于全局坐标系 X 轴，顺时针） |
| `bearing_true` | 度（°） | 真实方位角（无噪声真值，用于算法性能评估） |
| `snr_meas` | 分贝（dB） | 测量信号的信噪比（估计值） |
| `target_x` | 米（m） | 目标的真实 X 坐标（全局坐标系） |
| `target_y` | 米（m） | 目标的真实 Y 坐标（全局坐标系） |
| `bearing_body_meas` | 度（°） | 载体坐标系下的方位角测量值（相对艏向） |
| `time` | 秒（s） | 时间戳（从 1 开始递增，等间隔） |

> **注**：方位角均以正北（或 X 轴正向）为 0°，顺时针为正；部分 `bearing_true` 为 0 表示该时刻真值未记录，使用时请按需筛选。

---

## 🎯 适用研究场景

- **纯方位目标跟踪（Bearing‑Only Tracking）**  
  利用 `bearing_meas` 和观测站位置 `(obs_x, obs_y)` 估计目标轨迹，可与 `target_x, target_y` 真值对比精度。

- **数据降噪与滤波**  
  结合 `bearing_meas` 和 `bearing_true`，验证卡尔曼滤波、粒子滤波、自适应滤波等算法的去噪性能。

- **信噪比影响分析**  
  利用 `snr_meas` 分析不同信噪比下方位测量误差的统计特性。

- **目标运动模型辨识**  
  根据目标位置序列 `(target_x, target_y)` 建立匀速、匀加速或机动模型。

---

## 📖 如果您在研究中使用了本数据集，请引用以下两篇相关论文：

```bibtex
@ARTICLE{QIU11418655,
  title={MPPI-DWIT: Robust Bearing-Only Target Tracking of Single AUV With Detection Sector Constraints}, 
  author={Qiu, Shaoxiong and Xu, Hongli and Wang, Junyi and Ru, Jingyu and Zhang, Wenrui and Wang, Jia},
  journal={IEEE Transactions on Automation Science and Engineering}, 
  year={2026},
  volume={23},
  number={},
  pages={6175-6189},
  doi={10.1109/TASE.2026.3669656}}

@article{QIU2026123409,
  title = {Dynamic target tracking and pursuit for single AUV with bearing-only constrained sonar},
  author = {Shaoxiong Qiu and Hongli Xu and Jingyu Ru and Wenrui Zhang},
  journal = {Ocean Engineering},
  volume = {343},
  pages = {123409},
  year = {2026},
  issn = {0029-8018},
  doi = {https://doi.org/10.1016/j.oceaneng.2025.123409},
  url = {https://www.sciencedirect.com/science/article/pii/S0029801825030926}}
