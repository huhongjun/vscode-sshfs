# README

## intro

    git clone git@github.com:huhongjun/vscode-sshfs.git

## install nodejs

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
    
    source ~/.bashrc
    nvm list-remote
    nvm install v10.24.1 # 11.13,10.12
    nvm list
    nvm use v10.24.1
    nvm install v12.22.1 && nvm use v12.22.1
    node -v
    nvm use v12.22.4

    //.npmrc
    package-lock=false
    registry=https://registry.npm.taobao.org

## install yarn

    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

    sudo apt update
    sudo apt install --no-install-recommends yarn
    yarn --version

## debug

    mkdir -p ~/node_modules/sshfs && ln -s ~/node_modules/sshfs node_modules
    mkdir -p ~/node_modules/sshfs_webview && ln -s ~/node_modules/sshfs/webview node_modules

    sudo rm -rf node_modules/*
    sudo rm -rf webview/node_modules/*
    nvm use v12.22.1
    yarn install
    cd webview && yarn install

    #[.vscode/launch.json] Terminal -> Run Task ... -> Extension - Watch All
    #[.vscode/tasks.json] F5 Ctrl+Shift+P -> SSH FS

## note
