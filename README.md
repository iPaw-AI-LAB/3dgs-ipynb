# 实验用 3dgs-ipynb

## 运行
按照官方说明配好环境后
一键运行/root/autodl-tmp/train_3dgs.ipynb
即可看到训练流程

# 说明
render.py还没拆解
### 可微分渲染函数render.py（调用cuda）
autodl-tmp/gaussian-splatting/submodules/diff-gaussian-rasterization/diff_gaussian_rasterization/__init__.py

调用了autodl-tmp/gaussian-splatting/submodules/diff-gaussian-rasterization/rasterize_points.cu 的 RasterizeGaussiansCUDA （前向传播）

RasterizeGaussiansCUDA 函数调用了cuda写的前向传播 autodl-tmp/gaussian-splatting/submodules/diff-gaussian-rasterization/cuda_rasterizer/forward.cu 

RasterizeGaussiansBackwardCUDA （反向传播）

RasterizeGaussiansBackwardCUDA 函数调用了cuda写的前向传播 autodl-tmp/gaussian-splatting/submodules/diff-gaussian-rasterization/cuda_rasterizer/backward.cu
