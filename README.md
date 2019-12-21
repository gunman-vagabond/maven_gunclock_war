# maven GunClock

GunClock for maven.


## ���s���@

    $ git clone https://github.com/gunman-vagabond/maven_gunclock_war
    $ cd maven_gunclock_war
    $ mvn package

    �� target/gunman.war ����������܂�

## memo

���v���W�F�N�g�̐���(mvn��)

    % mvn archetype:generate -DgroupId=com.gunman -DartifactId=web-app -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false


��pom.xml

-------------------------------
    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
      <modelVersion>4.0.0</modelVersion>
      <groupId>com.gunman</groupId>
      <artifactId>web-app</artifactId>
      <packaging>war</packaging>
      <version>1.0-SNAPSHOT</version>
      <name>web-app Maven Webapp</name>
      <url>http://maven.apache.org</url>
      <dependencies>
        <dependency>
          <groupId>junit</groupId>
          <artifactId>junit</artifactId>
          <version>3.8.1</version>
          <scope>test</scope>
        </dependency>
     
     ��<dependency>��ǉ��Bversion��3.1.0�ɂ��Ă݂��Bweb.xml�����Ȃ��ł���Ă݂�B
     ��scope��provided�ɂ��邱�ƂŁAwar�ɓ���Ȃ�(�T�[�o�̂��g��)
        <dependency>
          <groupId>javax.servlet</groupId>
          <artifactId>javax.servlet-api</artifactId>
          <version>3.1.0</version>
          <scope>provided</scope>
        </dependency>
     
      </dependencies>
      <build>
     
     ��Name��ݒ�Bwar�̃t�@�C�����ɂȂ����B
        <finalName>gunclock</finalName>
     
     ��plugins��ǉ��Bversion��3.1.0�ɂ��Ă݂�Bweb.xml�����Ȃ��ł���Ă݂�B
        <plugins>
          <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-war-plugin</artifactId>
            <version>3.1.0</version>
          </plugin>
        </plugins>
    
      </build>
     </project>

��web.xml
- servlet 3.0 �� web.xml �ɂ���B
- Servlet�Ɋւ���L�q�́A��؂��Ȃ���OK�B
-------------------------
     <?xml version="1.0" encoding="UTF-8"?>
     
     <web-app xmlns="http://java.sun.com/xml/ns/javaee"
	      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	      xsi:schemaLocation="http://java.sun.com/xml/ns/javaee 
	      http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd"
	      version="3.0">
     </web-app>
-------------------------


���A�N�Z�X
     http://xxxx:8080/gunclock/gunclock

- ��ڂ�gunclock��war�t�@�C����
- �Q�ڂ�gunclock�̓A�m�e�[�V�����ŏ��������O


