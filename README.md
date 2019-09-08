# building.mrJar.modules

Building Java 9 Modules with mrJar — The Gradle Guide's Fully-modular Java 9 Storyteller Application

## WTF is This?

A complete working project that demonstrates how to use [*the lingocoder mrJar Gradle plugin*](http://bit.ly/mrJar). Using ***mrJar*** makes it easy to compile a project consisting of a set of collaborating, loosely-coupled [*Java 9<sup>+</sup> JPMS modules*](http://bit.ly/SoTmS). Going one step further than other plugins, ***mrJar*** can also package your modules into separate Modular Multi-Release JAR File (*MRJAR*) distributable artifacts. No other Gradle plugin currently exists (*neither from Gradle nor from the community*) that can create Modular MRJAR Files.

The source code in this demonstration project is essentially a fork of [*Gradle's companion code*](http://bit.ly/BldJ9Mods) to their excellent [*Building Java 9 Modules*](http://bit.ly/BldJ9Guide) User Guide. Changes in this project include modifications to the *`build.gradle`* files to make them 1) applicable to the ***mrJar*** plugin. And 2) compatible with my preferred IDE. Those changes made the build files significanly simpler and more concise. Aside from those cosmetic differences, none of the actual source code of Gradle's demo has been changed in this demo. The functionality in this demo is identical to the original on which it's based.

## What Will I Learn From this Demo?
The most important take away from this *building.mrJar.modules* demo, is how easy ***mrJar*** makes it to compile and package Java 9<sup>+</sup> modular MRJAR Files. This project also demonstrates that using the ***mrJar*** Gradle plugin instead of the code-in-build-script approach proposed by Gradle's guide, will make your build files a whole lot less cluttered, a lot easier to read and more importantly, way easier to maintain. 

## How Do I Run the Demo?

1. Clone or download the project <br />
   • *`cd`* into the root folder where you cloned/unzipped the project
2. In a command line terminal, enter: *`./gradlew :check`* <br />
   • that will launch the tests
3. Or enter: *`./gradlew :assemble`* <br />
   • that will bundle all the individual subprojects into there individual Jigsaw/Java 9<sup>+</sup> modules <br />
   • examine any one of the modules with: *`jar -f pigs/build/libs/org.gradle.fairy.tale.pigs.jar --describe-module`* <br />
    ```
    org.gradle.fairy.tale.pigs jar:/lingocoder/building.mrJar.modules/pigs/build/libs/org.gradle.fairy.tale.pigs.jar/!module-info.class
    exports org.gradle.fairy.tale.pigs
    requires java.base mandated
    requires org.gradle.actors
    requires org.gradle.fairy.tale transitive
    requires org.gradle.fairy.tale.formula
    ```
4. Or enter: *`./gradlew :fairy:run`* <br />
   • that will run the Storyteller application module that consumes all the other five modules and print:

    ```
    Once upon a time, there lived the 3 little pigs, and the big bad wolf.
    the first little pig was lazy and built his house of straw.
    the second little pig was common and built his house of wood.
    ...
    the big bad wolf hyper-ventilated and died.
    And they all lived happily ever after.
    ...
    Once upon a time, there lived Goldilocks, and the 3 bears.
    ...
    Papa Bear said, 'Somebody has been sleeping in my bed.'
    Mama Bear said, 'Somebody has been sleeping in my bed.'
    ...
    Goldilocks ran out of the house at top speed to escape the 3 bears.
    And they all lived happily ever after.

    ...
    BUILD SUCCESSFUL in 19s
    14 actionable tasks: 14 executed

    ```   


## Where Can I Find Out More?

Check out [*the **mrJar** project site*](http://bit.ly/mrjarsite). You'll find more detailed usage instructions listed there. Additionally, I introduced the very first v0.0.1 release of ***mrJar*** to the Gradle Community in [*this Gradle Forums post*](http://bit.ly/mrJarNtro). On top of usage tips for ***mrJar***, that post also has some valuable discussions of Java 9<sup>+</sup> Modules in general. Plus knowledge shared from several others in the community. If you have questions or suggestions, that is one way to reach out. I might post more ***mrJar*** plugin version updates there.

<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />  
  
  
  
  
  
  
  
  
  
  
______
<sup><sup><sup><sup>*1*</sup></sup></sup></sup><sup>*The **mrJar** Gradle plugin itself, is not derived from any other existing plugin. The **mrJar** plugin is an original software design implementated from scratch.*</sup>


