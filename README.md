# set_gpu_fans_public
Controlling the fan speed of an NVIDIA GPU on a headless linux system requires spoofing a display.
This can be used to gain a few percent additonal performance, at the cost of increased noise.
For installation and usage, read the comments in cool_gpu.
ln -s /root/set-gpu-fans /opt/set-gpu-fans
ln -s /usr/bin/nvidia-smi /opt/bin/nvidia-smi
/root/set-gpu-fans/cool_gpu >& /root/set-gpu-fans/controller.log &

## temp of multi-gpu is individually obtained and adjusted 
```bash
Thu May 25 09:57:10 2023       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 515.65.01    Driver Version: 515.65.01    CUDA Version: 11.7     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ...  On   | 00000000:04:00.0 Off |                  N/A |
| 60%   37C    P2   113W / 350W |  23758MiB / 24576MiB |     25%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   1  NVIDIA GeForce ...  On   | 00000000:05:00.0 Off |                  N/A |
| 60%   46C    P2   110W / 350W |  23757MiB / 24576MiB |     21%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   2  NVIDIA GeForce ...  On   | 00000000:08:00.0 Off |                  N/A |
| 60%   44C    P2   113W / 350W |  23757MiB / 24576MiB |     18%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   3  NVIDIA GeForce ...  On   | 00000000:09:00.0 Off |                  N/A |
| 60%   49C    P2   113W / 350W |  23757MiB / 24576MiB |     25%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   4  NVIDIA GeForce ...  On   | 00000000:84:00.0 Off |                  N/A |
| 60%   44C    P2   114W / 350W |  23757MiB / 24576MiB |     28%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   5  NVIDIA GeForce ...  On   | 00000000:85:00.0 Off |                  N/A |
| 60%   43C    P2   108W / 350W |  23757MiB / 24576MiB |     20%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   6  NVIDIA GeForce ...  On   | 00000000:88:00.0 Off |                  N/A |
| 60%   43C    P2   114W / 350W |  23757MiB / 24576MiB |     19%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
|   7  NVIDIA GeForce ...  On   | 00000000:89:00.0 Off |                  N/A |
| 60%   44C    P2   113W / 350W |  23757MiB / 24576MiB |     24%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
```
