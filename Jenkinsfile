@Library('Shared_library2.0') _

pipeline{
    agent any

    stages{

        stage('Git checkout'){

         steps{

            script{

                gitcheckout{
                 branch: "main"
                  url: "https://github.com/mateenshaik/Aws_project2.git"
            }
            }
        }
    }
 }
}