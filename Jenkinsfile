
pipeline{
  agent any
  tools { 
    maven '3.6.0'
    jdk 'java1.8.0'
  }
  stages {
    stage('Build') {
      steps {
      
        sh "mvn -B -DskipTests clean package"
      }
    }
    stage('Deploy') {
      steps {
        sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
      }
    }
    stage('Test') {
      steps {
      sh 'mvn test'
      }
    }
  }
}
