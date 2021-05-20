# colab-ffmpeg-cuda

FFmpeg build with CUDA support for Ubuntu (especially for Google Colab) with pre-built required binaries.

---

## Set Up

**Important:** You have to change the runtime type and use GPU hardware accelerator. If you have not done it, [check it below](#change-runtime-type-hardware-accelerator):

1. Clone the repository

```bash
# You need to prepend a `!` to execute a shell command in Goole Colab or Jupyter
!git clone https://github.com/fritolays/colab-ffmpeg-cuda.git
```

2. Copy all the pre-built binaries from `./colab-ffmpeg-cuda/bin/` to `/usr/bin/` (**Recommended**)

```bash
!cp -r ./colab-ffmpeg-cuda/bin/. /usr/bin/
```

3. Check the installed `ffmpeg` version

```bash
!ffmpeg -version
# Congratulations, ffmpeg with cuda support is installed!
```

### Is it not working?

If you are having trouble with the pre-built binaries, buid the binaries from scratch (**It may take more than half an hour**)

```bash
!chmod +x ./colab-ffmpeg-cuda/build
!./colab-ffmpeg-cuda/build --build
```
There you go, ffmpeg with the required binaries should be installed to `/usr/bin`.

---

## Change Runtime Type (Hardware Accelerator)

1. Go to `Runtime` on top-left options

<p align="center">
<img alt="Goto runtime" title="Goto runtime" src="./assets/goto_runtime.png" width="600" > 
</p>

2. Then go to `Change runtime type`

<p align="center">
<img alt="Goto runtime -> Change runtime type" title="Goto runtime -> Change runtime type" src="./assets/goto_runtime_then_goto_change_runtime_type.png" width="600" > 
</p>

3. Set `Hardware accelerator` type to `GPU`

<p align="center">
<img alt="Goto runtime -> Change runtime type -> Set hardware accelerator type to GPU" title="Goto runtime -> Change runtime type -> Set hardware accelerator type to GPU" src="./assets/set_hardware_accelerator_gpu.png" width="600" > 
</p>
