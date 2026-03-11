pipeline {
    agent { label 'slave' }

    parameters {
      choice choices: ['DEV', 'Prod'], description: 'choose environment', name: 'ENV'
      string defaultValue: '1.0.0', description: 'selecting the version', name: 'Version', trim: true
    }

    stages {

        stage("Working with variables") {
            steps {
                script {
                    def subject = "Jenkins"
                    def batchno = 4
                    println "The subject name is $subject and batcno is $batchno"
                }
            }
        }
        /* consume default variables */
        stage("Working with env-variables") {
            steps {
                script {
                    println "The Build Number: ${env.BUILD_NUMBER}"
                    println "Job Name: ${env.JOB_NAME}"
                    println "Workspace: ${env.WORKSPACE}"
                    echo "Branch: ${env.BRANCH_NAME}"

                        /* consume parameters variables */
                    println "the selected env is ${params.ENV}"
                    println "version is ${params.Version}"
                }
            }
        }

    }
}
