@Library('Shared_library2.0') _

pipeline{
    agent any

    stages{

        stage('Git checkout'){

         steps{

            script{

                gitCheckout{
                 branch: "main"
                  url: "https://github.com/mateenshaik/Aws_project2.git"
            }
            }
        }
    }
 }
}