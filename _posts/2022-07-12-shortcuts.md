---
toc: true
layout: post
description: Useful commands, libraries I use to make (some) everyday coding simple.
categories: [setup, code]
title: Dev Setup
---

My programming language of choice has mostly been Python lately, with dev both on Linux and Windows (and WSL) - both when I'm working on personal and professional projects. While some of it keeps me awake for quite a long time based on the criticality of the project, it becomes essential that the tools and commands I use are handy, ubiquitous and uniform across my machines. This post showcases some of these and will be updated continuously. 

# Key Principles

1. Most of my setup follows some of the key learnings I've had here, [here]({% post_url 2022-08-15-research_code %}).

# .bashrc 

{% include info.html text="Appended to the end of file." %}

Pre-req: `pip install gpustat` (for gpu machines only)


```bash
alias dc='docker-compose'
alias dbuild='docker build . -t'
alias sbc='source ~/.bashrc'
addalias() {
    echo "alias ${1}" >> $HOME/.bash_aliases
} #Source: https://unix.stackexchange.com/a/153978

alias conda-dump='conda env export --no-builds | grep -v "^prefix: " > environment.yml' #dumps conda environment to environment.yml

alias gpuwatch='gpustat -i 5 -p'
alias killgpuproc='nvidia-smi | grep "python" | awk "{ print $5 }" | xargs -n1 kill -9'
alias killcpuproc='ps aux | grep "python" | awk "{ print $5 }" | xargs -n1 kill -9'

alias wandbstop='wandb disabled' #for debugging
```

> `addalias` is particularly useful to quickly shift to projects in different folders.

# Python

## Libraries and Frameworks

1. [Numba](https://numba.pydata.org/) - makes things go vroom.
2. [Fastcore](https://github.com/fastai/fastcore) - reduces regular boilerplate by quite a lot.
3. [Streamlit](https://streamlit.io) - host dashboard to present to multiple people asynchronously and remotely.
4. [Ray](https://ray.io) - large scale distributed code.
5. [Dask](https://dask.org) - host cluster on remote machines and send compute to these clusters. fast pandas alternative
5. [Sphinx](https://www.sphinx-doc.org/en/master/) - build and host documentation
6. [FastAPI](https://fastapi.tiangolo.com/) - web framework of choice
7. [PostgreSQL](https://postgresql.org) - database of choice
9. [sqlalchemy](https://sqlalchemy.org) - ORM of choice
10. [Hydra](https://hydra.cc) - config management
11. [Wandb](https://wandb.ai)/[mlflow](https://mlflow.org) - experiment tracker personal/professional

