# Fine-tune-LLMS-with-grp
Fine-tune LLMs with GRPO algorithm video tutorial [link]()

List of Unsloth notebooks [link](https://docs.unsloth.ai/get-started/unsloth-notebooks)


## Environement set-up (Windows)

Setting up the environment for this notebook depends heavily on you PC configuration:

First, Unsloth only supports `python=3.10, 3.11, 3.12`
Then the environment setup is different depending on whether you have conda or not (refer to [unsloth docs](https://docs.unsloth.ai/get-started/installing-+-updating)).
1. You need to download the CUDA Toolkit version that is supported by your GPU.
2. Based on the cuda version you have, you need then to install the required libraries with the correct versions.

**Note:** If you're on windows and you want to use vLLM for fast inference. You need then to work with WSL and you can then follow the Linux installation from the [unsloth docs](https://docs.unsloth.ai/get-started/installing-+-updating).


If your GPU supports CUDA v 12.4, then you can clone my conda enironment, either from the .yaml file or by copying the following commands.

```
conda create --name unsloth_env  python=3.11
pip install torch==2.5.1 torchvision --index-url https://download.pytorch.org/whl/cu124
pip install -U xformers==0.0.28.post3 --index-url https://download.pytorch.org/whl/cu124
pip install https://github.com/woct0rdho/triton-windows/releases/download/v3.1.0-windows.post9/triton-3.1.0-cp311-cp311-win_amd64.whl
pip install "unsloth[colab-new] @ git+https://github.com/unslothai/unsloth.git"
pip install --no-deps peft accelerate bitsandbytes
pip install git+https://github.com/huggingface/trl.git@e95f9fb74a3c3647b86f251b7e230ec51c64b72b
pip install diffusers[torch] transformers
```