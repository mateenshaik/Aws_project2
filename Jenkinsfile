@Library('Shared_library2.0') _

pipeline {
    agent any

    parameters{

        choice(name: 'actio', choice: 'create\ndelete', description: 'choose create/Destroy')
    }

    stages {
         
        stage('Git checkout') {
             when { expression { pram.action == 'create'} }
            steps {
                script {
                    gitCheckout(branch: "main", url: "https://github.com/mateenshaik/Aws_project2.git")
                }
            }
        }
        stage('Unit Test maven'){
            when { expression { pram.action == 'create'} }
            steps{
                script{
                    mvnTest()
                }
            }
        }
        stage('Integration test'){
            when { expression { pram.action == 'create'} }
            steps{
                script{
                    mvnintegrationTest()
                }
            }
        }
         stage('static code Analysis: sonarqube'){
            when { expression { pram.action == 'create'} }
            steps{
                script{
                     StaticCodeAnalysis()
                }
            }
        }
    }
}


