---
# NeuroDynamics-Control (神经动力学控制)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
**A Computational Framework for Closed-Loop rTMS Parameter Optimization**  
**基于闭环rTMS参数优化的计算框架**

---

### 中文版
#### 核心功能
 本仓库包含：
1. **多模态数据融合**：EEG-fMRI-HRV时序对齐算法（NeuroConv扩展版）
2. **神经动力学建模**：基于BrainPy的丘脑皮质振荡模型（含自主神经反馈模块）
3. **MPC控制器**：实时rTMS参数优化算法（采样周期200ms）

#### 快速开始
```python
# 安装依赖
pip install neurompc==0.1.alpha

# 运行示例
from neurompc import Controller
ctrl = Controller(config="default.yaml")
ctrl.real_time_loop()
```

#### 技术亮点
 创新特性：
- 混合精度状态估计（FP16/FP32自动切换）
- 基于HRV的自主神经状态量化模块
- 刺激参数安全约束系统（符合IEC 60601-2-6）

#### 路线图
 2024 Q3：
- [ ] 开源基础模型架构
- [ ] 发布preprint论文
- [ ] 集成索尼EEG头环SDK

---

### English Version
#### Core Features
 This repository contains:
1. **Multimodal Data Fusion**: EEG-fMRI-HRV temporal alignment (NeuroConv Extended)
2. **Neural Dynamics Modeling**: Thalamocortical oscillation model with autonomic feedback (BrainPy-based)
3. **MPC Controller**: Real-time rTMS parameter optimization (200ms sampling cycle)

#### Quick Start
```python
# Installation
pip install neurompc==0.1.alpha

# Run demo
from neurompc import Controller
ctrl = Controller(config="default.yaml")
ctrl.real_time_loop()
```

#### Technical Highlights
 Innovative Features:
- Mixed-precision state estimation (FP16/FP32 auto-switching)
- HRV-based autonomic state quantifier
- Stimulation safety constraint system (IEC 60601-2-6 compliant)

#### Roadmap
 2024 Q3:
- [ ] Release core model architecture
- [ ] Publish preprint paper
- [ ] Integrate Sony EEG Headset SDK

---

### 参与贡献 | Contribution
 联系: tangrunxuan.phd@outlook.com  
 开发文档: [docs.neurompc.org](http://docs.neurompc.org) (建设中)

```markdown
# 协作流程 | Workflow
1. Fork本仓库
2. 创建特性分支 (git checkout -b feature/AmazingFeature)
3. 提交变更 (git commit -m 'Add some AmazingFeature')
4. 推送分支 (git push origin feature/AmazingFeature)
5. 发起Pull Request
```

---

### 许可协议 | License
本项目采用 **[MIT License](LICENSE)** 授权  
临床数据子模块遵循 **[HIPAA合规协议](compliance/HIPAA.md)**

