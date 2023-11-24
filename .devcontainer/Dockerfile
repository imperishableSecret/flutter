FROM "mcr.microsoft.com/devcontainers/base:bullseye"
# Install the xz-utils package
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y zsh-autosuggestions zsh-syntax-highlighting zoxide exa neofetch

USER vscode
RUN git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
COPY .zshrc /home/vscode/.zshrc
COPY .p10k.zsh /home/vscode/.p10k.zsh

USER root
RUN chown -R vscode /home/vscode/