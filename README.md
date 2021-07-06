## CICFlowMeter v4.0 - Installation Instructions
> The official repository on github is : `https://github.com/ahlashkari/CICFlowMeter`

> To properly compile CICFlowMeter you need Eclipse or IntelliJ IDEA (The latter is recommended)

---

### Installation steps for Ubuntu 20.04 (As of 19.04.2021)

1. Installation of pre-requisites
   - `sudo apt update`
   - `sudo apt install maven openjdk-11-jdk -y`

2. Clone repository
   - `git clone https://github.com/ahlashkari/CICFlowMeter`
   - `cd CICFlowMeter`

3. Maven-install jnetpcap (included in the repository)
   - `cd jnetpcap/linux/jnetpcap-1.4.r1425`
   - `mvn install:install-file -Dfile=jnetpcap.jar -DgroupId=org.jnetpcap -DartifactId=jnetpcap -Dversion=1.4.1 -Dpackaging=jar`

4. IntelliJ IDEA
   - Download and install IntelliJ IDEA. 
   - Open the git-cloned folder as a gradle project.
   - Ignore the warnings and let it index the project.

5. Run the project
   - Open a terminal inside IntelliJ IDEA
   - `sudo bash`
   - `./gradlew run`
   - Press Ctrl+Enter to run the command and not just Enter !

6. Build the project for native use
   - Open a terminal inside IntelliJ IDEA
   - `sudo bash`
   - `./gradlew distZip`
   - Press Ctrl+Enter to run the command and not just Enter !
   - The zip will be at ./build/distributions

---

### Installation steps for Windows 10 (As of 19.04.2021)

1. Download and install IntelliJ IDEA

2. Install any java version. 

3. Clone repository

4. Open the CICFlowMeter folder as a gradle project

5. Ignore the warning and let it index the project

6. Open terminal in IntelliJ IDEA
   - `mvn install:install-file -Dfile=jnetpcap.jar -DgroupId=org.jnetpcap -DartifactId=jnetpcap -Dversion=1.4.1 -Dpackaging=jar`
   - Press Ctrl+Enter to run the command and not just Enter !

7. Run the project
   - Right-Click at 'gradlew'
   - Run
   - Open a terminal in IntelliJ IDEA
   - `gradlew run`
   - Press Ctrl+Enter to run the command and not just Enter !

8. Build the project for native use
   - Open a terminal 
   - `gradlew distZip`
   - Press Ctrl+Enter to run the command and not just Enter !
   - The zip will be at ./build/distributions
