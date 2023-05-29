// @Library('Shared_library2.0') _

// pipeline{
//     agent any

//     stages{

//         stage('Git checkout'){

//          steps{

//             script{

//                 gitCheckout{
//                  branch: "main"
//                   url: "https://github.com/mateenshaik/Aws_project2.git"
//             }
//             }
//         }
//     }
//  }
// }
@Library('Shared_library2.0') _
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import groovy.json.*
import java.net.URL

pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                script {
                    gitCheckout(branch: "main", url: "https://github.com/mateenshaik/Aws_project2.git")
                }
            }
        }
    }
}

// def gitCheckout(Map stageParams) {
//     checkout([
//         $class: 'GitSCM',
//         branches: [[name: stageParams.branch]],
//         userRemoteConfigs: [[url: stageParams.url]]
//     ])
// }
