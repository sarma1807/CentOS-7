### Install & Configure Oracle JDK & JRE

##### Download Oracle JDK & JRE : http://www.oracle.com/technetwork/java/javase/downloads/index.html

---

[root@metalgear ~]# ` cat /etc/centos-release ` <br>
CentOS Linux release 7.2.1511 (Core) <br><br>

[root@metalgear ~]# ` uname -a ` <br>
Linux metalgear.mydomain 3.10.0-327.10.1.el7.x86_64 #1 SMP Tue Feb 16 17:03:50 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux

---

[root@metalgear ~]# ` java -version ` <br>
openjdk version "1.8.0_71" <br>
OpenJDK Runtime Environment (build 1.8.0_71-b15) <br>
OpenJDK 64-Bit Server VM (build 25.71-b15, mixed mode) <br><br>

[root@metalgear ~]# ` javac -version ` <br>
bash: javac: command not found... <br>
Similar command is: 'java' <br>

#### CentOS 7 by default comes with OpenJDK Java Runtime Environment.

---

#### Install Oracle JDK & JRE 1.8 update 74

[root@metalgear ~]# ` rpm -ivf jdk-8u74-linux-x64.rpm ` <br>
Preparing packages... <br>
jdk1.8.0_74-2000:1.8.0_74-fcs.x86_64 <br>
Unpacking JAR files... <br>
	tools.jar... <br>
	plugin.jar... <br>
	javaws.jar... <br>
	deploy.jar... <br>
	rt.jar... <br>
	jsse.jar... <br>
	charsets.jar... <br>
	localedata.jar... <br>
	jfxrt.jar... <br><br>

[root@metalgear ~]# ` rpm -ivf jre-8u74-linux-x64.rpm ` <br>
Preparing packages... <br>
jre1.8.0_74-1.8.0_74-fcs.x86_64 <br>
Unpacking JAR files... <br>
	plugin.jar... <br>
	javaws.jar... <br>
	deploy.jar... <br>
	rt.jar... <br>
	jsse.jar... <br>
	charsets.jar... <br>
	localedata.jar... <br>
	jfxrt.jar... <br> <br>

---

#### Update Alternatives to Point Java and JavaC to Oracle JDK & JRE 1.8 update 74

[root@metalgear ~]# ` update-alternatives --config java ` <br>

`
There are 3 programs which provide 'java'. <br>

  Selection    Command
-----------------------------------------------
*+ 1           /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.71-2.b15.el7_2.x86_64/jre/bin/java
   2           /usr/java/jdk1.8.0_74/jre/bin/java
   3           /usr/java/jre1.8.0_74/bin/java

Enter to keep the current selection[+], or type selection number: 3
`
#### Select 3 to point Java (JRE) to Oracle JRE 1.8 update 74

---

[root@metalgear ~]# update-alternatives --config java

There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
*  1           /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.71-2.b15.el7_2.x86_64/jre/bin/java
   2           /usr/java/jdk1.8.0_74/jre/bin/java
 + 3           /usr/java/jre1.8.0_74/bin/java

Enter to keep the current selection[+], or type selection number: 3

[root@metalgear ~]# update-alternatives --config javac

There is 1 program that provides 'javac'.

  Selection    Command
-----------------------------------------------
*+ 1           /usr/java/jdk1.8.0_74/bin/javac

Enter to keep the current selection[+], or type selection number: 1

[root@metalgear ~]# update-alternatives --config javac

There is 1 program that provides 'javac'.

  Selection    Command
-----------------------------------------------
*+ 1           /usr/java/jdk1.8.0_74/bin/javac

Enter to keep the current selection[+], or type selection number: 1

[root@metalgear ~]# java -version
java version "1.8.0_74"
Java(TM) SE Runtime Environment (build 1.8.0_74-b02)
Java HotSpot(TM) 64-Bit Server VM (build 25.74-b02, mixed mode)

[root@metalgear ~]# javac -version
javac 1.8.0_74

