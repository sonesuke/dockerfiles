FROM debian:latest

# install exa fdfind rg
RUN apt-get update \
    && apt-get install -y \
            exa \
            fd-find \
            ripgrep \
            rpm \
            wget \
            curl \
            sudo \
            less \
            fzf \
    && echo "alias fd='fdfind'" >> ~/.bashrc


# intall procs
RUN wget https://github.com/dalance/procs/releases/download/v0.9.20/procs-0.9.20-1.x86_64.rpm \
    && rpm -i procs-0.9.20-1.x86_64.rpm \
    && rm *.rpm

# install bat
RUN wget https://github.com/sharkdp/bat/releases/download/v0.12.1/bat-musl_0.12.1_amd64.deb \
    && dpkg -i bat-musl_0.12.1_amd64.deb \
    && rm *.deb

# install zoxide
RUN curl --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/ajeetdsouza/zoxide/master/install.sh | sh \
    && echo 'eval "$(zoxide init bash)"' >> ~/.bashrc

