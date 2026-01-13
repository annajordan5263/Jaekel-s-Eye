# 杰克尔之眼 (Jaekel's Eye, JE)

## 🌟 项目概述

基于早泥盆世顶级掠食者 Jaekelopterus 的仿生智能机器人系统，融合高性能计算、仿真模拟和人机协同技术，用于古海洋生态系统重建和地质探索。

## 🚀 快速开始

### 环境要求
- Ubuntu 20.04+ / Windows 10+
- CUDA 12.0+ (推荐NVIDIA RTX 4090)
- Python 3.9+
- CMake 3.16+
- MySQL 8.0+

### 安装步骤
```bash
# 1. 克隆项目
git clone https://github.com/jaekels-eye/jaekels_eye.git
cd jaekels_eye

# 2. 安装Python依赖
pip install -r requirements.txt

# 3. 编译C++核心
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release -DUSE_CUDA=ON -DUSE_MPI=ON
make -j$(nproc)

# 4. 启动服务
cd ../api
uvicorn main:app --host 0.0.0.0 --port 8000