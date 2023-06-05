@Library('Shared_library2.0') _

pipeline {
    agent any

    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'choose create/Destroy')
    }

    stages {
         
        stage('Git checkout') {
             when { expression { prams.action == 'create'} }
            steps {
                script {
                    gitCheckout(branch: "main", url: "https://github.com/mateenshaik/Aws_project2.git")
                }
            }
        }
        stage('Unit Test maven'){
            when { expression { prams.action == 'create'} }
            steps{
                script{
                    mvnTest()
                }
            }
        }
        stage('Integration test'){
            when { expression { prams.action == 'create'} }
            steps{
                script{
                    mvnintegrationTest()
                }
            }
        }
         stage('static code Analysis: sonarqube'){
            when { expression { prams.action == 'create'} }
            steps{
                script{
                     StaticCodeAnalysis()
                }
            }
        }
    }
}


