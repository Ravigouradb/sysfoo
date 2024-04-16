pipeline {
  agent any
  tools{
    maven 'Maven 3.6.3'
  }
  stages{
      stage("build"){
          steps{
              echo 'compiling the code..'
              sh 'mvn compile'
              sleep 3
          }
      }
      stage("runtest"){
          steps{
              echo 'run automation ....'
             sh 'mvn clean test'
              sleep 9
          }
      }
      stage("create_pkg"){
          steps{
              echo 'create pkg...'
              sh 'mvn package -DskipTests'
              sleep 5
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
