pipeline {
    agent any
    stages {
        stage ('clone') {
           steps{
              git branch: 'master',url: 'https://https://github.com/wakaleo/game-of-life.git'
           }
        }
        stage('build and test'){
            steps{
                sh 'mvn clean package'
                sh 'echo "build run"
                archiveArtifacts artifacts: '**/target/*.war', fingerprint: true
                       } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
         }
     }     
