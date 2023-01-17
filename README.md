# CUDA installation on WSL2 Ubuntu 20.04 and Windows11 
---

**Motivation Link of this Repo: [Link](https://2022.ubucon.asia/sessions/cuda-with-wsl2-and-ubuntu-without-docker/)**

---

**NVIDIA CUDA Installation on WSL2 Ubuntu-20.04 on Windows11**

---

**Overall View:**

---

**Main Instruction Guide: https://docs.nvidia.com/cuda/wsl-user-guide/index.html**     

---

![img](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image002.jpg)

**Step 1**: **Enable WSL2.**

**Step 2**: Install **Ubuntu** on **WSL2** or **Ubuntu-20.04 from Microsoft Store.**

**Step 3: Install Nvidia Driver and Cuda Toolkit on Windows 11.**

**3.1 Nvidia Driver for Windows11:**

[**https://developer.nvidia.com/cuda/wsl**](https://developer.nvidia.com/cuda/wsl)

[**https://www.nvidia.com/Download/index.aspx**](https://www.nvidia.com/Download/index.aspx)

![img](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image004.jpg)                  

**3.2 Download CUDA Toolkit Download:**

[**https://developer.nvidia.com/cuda-downloads**](https://developer.nvidia.com/cuda-downloads)

![Graphical user interface  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image006.jpg)

**Step4: Follow the Guide of this Link :** [**https://docs.nvidia.com/cuda/wsl-user-guide/index.html**](https://docs.nvidia.com/cuda/wsl-user-guide/index.html)

4.1 **Open Ubuntu from start menu**

![img](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image008.jpg)

4.2 **Ubuntu-20.04 Terminal Looks Like this:**

![Background pattern  Description automatically generated with medium confidence](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image010.jpg)
 

**4.3 Commands to execute on the above terminal:**

**Step1 : Execute the below command**

```bash
sudo apt-key del 7fa2af80
```



![Text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image012.jpg)

**Step 2: Open this link :** [**https://developer.nvidia.com/cuda-downloads**](https://developer.nvidia.com/cuda-downloads) **and select below option.**

![Graphical user interface, text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image014.jpg)

 

 

 

**Step3: Copy Above All command and paste it on Ubuntu Terminal**

![Text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image016.jpg)

**and end will be look like this.**

![Text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image018.jpg)

**Step4: For checking local GPU on Ubuntu Terminal Type nvidia-smi and it will display gpu configuration**

![Text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image020.jpg)

**Step5: Now time to check the Docker terminal test of Nvidia.**

**Docker Command:** 

```bash
docker run --gpus all nvcr.io/nvidia/k8s/cuda-sample:nbody nbody -gpu -benchmark
```

 

![img](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image022.jpg)

**Step 6: Now Run the tensorflow docker file and run on GPU.**

```bash
docker run --gpus all -it --name tfgpu -p 8888:8888 -v ${PWD}:/tf/notebooks tensorflow/tensorflow:latest-gpu-jupyter
```



![Text  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image024.jpg)

![Graphical user interface, text, application  Description automatically generated](https://raw.githubusercontent.com/ashishpatel26/Cuda-installation-on-WSL2-Ubuntu-20.04-and-Windows11/main/Images/clip_image026.jpg)
