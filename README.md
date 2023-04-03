# macos-setup
Default setup on MacOS for software development

## Terminal
```shell
brew install direnv
```

Add to `~/.zshrc`
```shell

# node version manager
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# pyenv
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# pyenv-virtualenv
if which pyenv-virtualenv-init > /dev/null; then eval "$(pyenv virtualenv-init -)"; fi

# java
export JAVA_HOME=`/usr/libexec/java_home -v 18.0.2.1`

# Load Angular CLI autocompletion.
source <(ng completion script)

# python poetry
export POETRY_HOME="~/Library/Application Support/pypoetry"
export PATH="/Users/ramandeepsingh/.local/bin:$PATH"

# Kubernetes
export USE_GKE_GCLOUD_AUTH_PLUGIN=Trueexport PATH="$HOME/.jenv/bin:$PATH"
eval "$(jenv init -)"

# add direnv
eval "$(direnv hook zsh)"
```

## Runtimes
### Node
...

### Java
1. Instal jEnv
    ```
    brew install jenv
    mkdir ~/.jenv
    mkdir ~/.jenv/versions
    ```

2. Install openJDK versions
    ```
    brew install openjdk@19
    brew install openjdk@18
    brew install openjdk@17
    brew install openjdk@11

    sudo ln -sfn /opt/homebrew/opt/openjdk@19/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
    sudo ln -sfn /opt/homebrew/opt/openjdk@18/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
    sudo ln -sfn /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
    sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
    ```

3. Install openJDK 8 for Apple M1

    Download .pkg file from [Adoptium](https://adoptium.net/de/temurin/releases/?version=8).

4. Register openJDK versions
    ```
    jenv add /opt/homebrew/opt/openjdk@19
    jenv add /opt/homebrew/opt/openjdk@18
    jenv add /opt/homebrew/opt/openjdk@17
    jenv add /opt/homebrew/opt/openjdk@11
    jenv add /Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home
    ```

5. Select active openJDK version
    ```
    jenv versions
    jenv global [...]
    ```

### Python
...
