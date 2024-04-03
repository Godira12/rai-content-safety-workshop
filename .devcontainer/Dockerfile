FROM mcr.microsoft.com/devcontainers/miniconda:0-3
# System packages 
RUN apt-get update && apt-get install -y curl

# needed for build_mlindex
RUN apt update && apt install -y fuse

# Install mamba
RUN conda install -n base -c conda-forge mamba

#Choose your version of azcli
RUN echo "pip install azure-cli" | bash
#Choose your version of ml cli
RUN echo "az extension add -n ml" | bash 
RUN echo "pip install azure-ml --extra-index-url https://azuremlsdktestpypi.azureedge.net/sdk-cli-v2" | bash
