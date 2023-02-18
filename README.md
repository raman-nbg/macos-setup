# macos-setup
Default setup on MacOS for software development

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
