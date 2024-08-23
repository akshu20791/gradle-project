pipeline{
    agent any
    stages{
        stage('github validation'){
          steps{
                 git url: 'https://github.com/akshu20791/gradle-project'
                 sh "chmod +x gradlew"
          }
        }
      stage('gradle build'){
          steps{
                sh "./gradlew jar"
          }
        }
       stage('deply'){
          steps{
                sh "java -jar build/libs/BuildSystemBasics-1.0-SNAPSHOT.jar"
          }
        }
    }     
  }
  
