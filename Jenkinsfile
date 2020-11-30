pipeline {
    agent any
    stages {
        stage ('Build') {
           steps{
              git url: 'https://https://github.com/wakaleo/game-of-life.git'
              withMaven {
            sh "mvn clean verify"
           } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
         }
     }     
  }
}    
