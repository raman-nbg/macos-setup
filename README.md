# macos-setup
Default setup on MacOS for software development

## Runtimes
### Node
...

### Java
- Download latest GA Version from https://jdk.java.net/
- Unpack downloaded file `tar -xf openjdk-17_macos-x64_bin.tar.gz`
- Move JDK to JavaVirtualMachines: `sudo mv jdk-17.jdk /Library/Java/JavaVirtualMachines/`
- Check installation `java -version`
- Set JAVA_HOME ``export JAVA_HOME=`/usr/libexec/java_home -v 18.0.2.1` ``

### Python
...
