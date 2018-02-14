# Docker image file that describes an Ubuntu16.04 image with PowerShell installed from Microsoft APT Repo

FROM microsoft/powershell:ubuntu16.04
LABEL maintainer="DSC Team" 

# Install dependencies and clean up
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
	apt-utils \
	apt-utils \
        libc6 \
        libcurl3 \
        ca-certificates \
        libgcc1 \
        curl \
        git
COPY G:\PowerShell-DSC-for-Linux\releaseBuild\Images\microsoft_dsc_ubuntu16.04\test.ps1 /

# Use PowerShell as the default shell
ENTRYPOINT [ "pwsh" ]
