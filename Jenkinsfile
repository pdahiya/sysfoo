pipeline {
  agent any
  tools {
    maven "Maven 3.6.3"
  }
  stages{
      stage("build"){
          steps{
              echo "compile"
              sh 'mvn compile'
              sleep 1
          }
      }
      stage("test"){
          steps{
            echo "test"
              sh 'mvn clean test'
              sleep 1
          }
      }
      stage("package"){
          steps{
            echo "package"
              sh 'mvn package -DskipTests'
              sleep 1
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
