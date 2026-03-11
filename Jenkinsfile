
pipeline {
    agent { label 'slave' }

    stages {
        stage("Working with variables") {
            steps {
                script {
                    def subject = "Jenkins"
                    def batchno = 4 
                    println "The subject name is $subject and batcno is $batchno"
                       }
                  }
              }                          }
        stage("Working with env-variables") {
            steps {
                script {
                    println "The Build Number: ${env.BUILD_NUMBER}"
                    println "Job Name: ${env.JOB_NAME}"
                    println "Workspace: ${env.WORKSPACE}" 
                    echo "Branch: ${env.BRANCH_NAME}"
                        }
                }
            }
    }
}



