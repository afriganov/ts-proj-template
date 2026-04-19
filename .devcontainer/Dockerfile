ARG VARIANT=24-bookworm
FROM  node:${VARIANT}

RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    curl \
    git \
    zsh \
    jq \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
 

RUN npm install -g typescript prettier pnpm

RUN chsh -s /usr/bin/zsh root
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" --unattended
