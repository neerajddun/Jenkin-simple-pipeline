pipeline {

  tools {
    maven 'Maven 3.9.4' // Name of Maven tool as configured in Jenkins
    jdk 'jdk 17'        // Name of JDK tool as configured in Jenkins
  }

  agent any

  stages {

    stage ('Checkout') {
      steps {
        // Check out the code from the specified Git repository
        git url: 'https://github.com/neerajddun/Jenkin-simple-pipeline.git', branch: 'main'
      }
    }

    stage ('Unit Test') {
      steps {
        // Run Maven unit tests
        sh 'mvn test'
      }
    }

    stage ('Build') {
      steps {
        // Build the Maven project
        sh 'mvn clean install'
      }
    }

    stage ('Deploy') {
      steps {
        sh 'echo "Deploy logic goes here "'
      }
    }

  }
}
