---
layout: page
title: Daily Cheat Sheet
permalink: /cheatsheet/
---

- [SSH-KeyGen](#ssh-keygen)
- [VSCode Snippets](#vscode-snippets)
- [NVIDIA Driver/CUDA/CUDNN](#nvidia-drivercudacudnn)


# SSH-KeyGen

```bash
ssh-keygen
ssh-keygen -t ed25519 -C "your_email@example.com"
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

# VSCode Snippets

```text
{
	// Place your snippets for python here. Each snippet is defined under a snippet name and has a prefix, body and 
	// description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the 
	// same ids are connected.
	// Example:
	// "Print to console": {
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
	"HEADER":{
		"prefix": "header",
			"body": [
			
			"#!/usr/bin/env python3",
			"# -*- encoding: utf-8 -*-",
			"\"\"\"",
			"@File    :   $TM_FILENAME",
			"@Time    :   $CURRENT_YEAR/$CURRENT_MONTH/$CURRENT_DATE $CURRENT_HOUR:$CURRENT_MINUTE:$CURRENT_SECOND",
			"@Author  :   liuchenhui",
			"@Contact :   jason_lchwork@163.com",
			"@Desc    :   None",
			"\"\"\"",
			""
		]
	}
}
```

# NVIDIA Driver/CUDA/CUDNN

- [CUDA ToolKit Latest Documentation](https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html)
- [Conda CUDA ToolKit Installation Documentation](https://anaconda.org/nvidia/cuda-toolkit)

> CUDA: 11.8
> Nvidia Driver: >=450.80.02

```bash
conda create -n pytorch201_cuda118 python=3.9
conda activate pytorch201_cuda118
conda install -c "nvidia/label/cuda-11.8.0" cuda-toolkit
nvcc --version
```