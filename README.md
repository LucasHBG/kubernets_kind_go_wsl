# kubernets_kind_go_wsl
Thats a HOW TO guide for using Kubernets (k8s) with GO installation and WSL.

## Step 1 - Download and install GO on WSL.
- Access GO's release versions at their website. [Link][go_website]
- Open your WSL terminal
- Type `wget https://go.dev/dl/[GO_VERSION_HERE].linux-amd64.tar.gz`
- After the download has finished type `sudo tar -xvf go1.20.5.linux-amd64.tar.gz`
- Move the directory to the local files: `sudo mv go /usr/local`
- Edit your `.bashrc`, `.zshrc` or similar with these settings:
    ```
      export GOROOT=/usr/local/go
      export GOPATH=$HOME/go
      export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
    ```
- Reload your bash, zsh etc configs or open a new terminal instance

## Step 2 - Kind installation
- Just type `go install sigs.k8s.io/kind@v0.19.0` but be aware that this is installing kind version 0.19.0
- For older or newer kind version go to [kind official website][kind_website]

## Step 3 - Create your cluster
- To create your cluster with kind type `kind create cluster`

[go_website]:https://go.dev/dl/
[kind_website]:https://kind.sigs.k8s.io
