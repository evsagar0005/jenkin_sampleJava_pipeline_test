HelloJenkins.java has sample java program to print hello Jenkins.



procedure:
have HelloJenkins.java on github with java code in it,
create ajava pipeline, connecting github rep to it.
have below pipeline code and run

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'javac HelloJenkins.java'
            }
        }
        stage('Run') {
            steps {
                sh 'java HelloJenkins'
            }
        }
    }
}



extra material:


Certainly! Let's create a simple **Java** program and set up a **Jenkins pipeline** to compile and run it. I'll guide you through the steps:

1. **Create a Simple Java Program**:
   - Let's create a basic Java program that prints "Hello, Jenkins!" to the console.
   - Save this code in a file named `HelloJenkins.java`:

```java
public class HelloJenkins {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins!");
    }
}
```

2. **Set Up Jenkins Pipeline**:
   - Open your Jenkins instance.
   - Create a new **Pipeline** job (or configure an existing one).
   - In the pipeline configuration, select "Pipeline script" or "Pipeline script from SCM" (if your code is in a Git repository).

3. **Write the Jenkins Pipeline Script**:
   - If you're using a pipeline script directly, use the following script:

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'javac HelloJenkins.java'
            }
        }
        stage('Run') {
            steps {
                sh 'java HelloJenkins'
            }
        }
    }
}
```

4. **Explanation**:
   - The pipeline has two stages: **Build** and **Run**.
   - In the **Build** stage, we compile the `HelloJenkins.java` file using `javac`.
   - In the **Run** stage, we execute the compiled program using `java`.

5. **Save and Build**:
   - Save your pipeline configuration.
   - Trigger a build by clicking "Build Now" or wait for it to run automatically (if you've set up triggers).

6. **View Console Output**:
   - Check the console output to see if the build and execution were successful.
   - You should see "Hello, Jenkins!" printed in the output.

That's it! You've created a simple Jenkins pipeline to compile and run a Java program. 🚀🔧

Learn more about Jenkins pipelines in the [official documentation](https://www.jenkins.io/doc/pipeline/tour/deployment/).¹²

Source: Conversation with Bing, 21/2/2024
(1) How to run a simple java file using Jenkins pipeline?. https://stackoverflow.com/questions/70915888/how-to-run-a-simple-java-file-using-jenkins-pipeline.
(2) How to compile and run a simple java file in jenkins on Windows. https://stackoverflow.com/questions/15020034/how-to-compile-and-run-a-simple-java-file-in-jenkins-on-windows.
(3) How to compile and run a simple java file in jenkins in windows. https://stackoverflow.com/questions/39942958/how-to-compile-and-run-a-simple-java-file-in-jenkins-in-windows.
(4) Build a Java app with Maven - Jenkins. https://www.jenkins.io/doc/tutorials/build-a-java-app-with-maven/.
