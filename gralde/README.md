# Gradle

------

Gradle 是以 Groovy 语言为基础，面向Java应用为主。基于DSL（领域特定语言）语法的自动化构建工具。


###  Could not run build action using Gradle distribution

[Could not run build action using Gradle distribution](http://www.quke.org/post/andriod-studio-gradle.html)

### 任何人获取代码后，不用安装gradle，就可以构建工程。

> 在项目根目录下，运行终端命令gradle wrapper，就会生成下面几个文件：
<pre>
project-root
    |-gradle
        |-wrapper
            |-gradle-wrapper.jar
            |-gradle-wrapper.properties
    |-gradlew
    |-gradlew.bat
gradlew, gradlew.bat 是支持多平台的gradle运行命令，通过gradlew，可以执行gradle构建任务。
如果运行时，发现系统没有对应版本的gradle，会通过gradle-wrapper.jar下载gradle-wrapper.properties中指定的gradle版本。这样的话，
任何人获取代码后，不用安装gradle，就可以构建工程。
gradle-wrapper.properties文件中指定的版本，就是运行gradle wrapper命令时的gradle版本。
当然，也可以手动指定别的版本，在根目录下build.gradle文件中添加:
<code>
task wrapper(type: Wrapper) {
    gradleVersion = '2.3'
}
<code>
再运行gradle wrapper。
<pre>
