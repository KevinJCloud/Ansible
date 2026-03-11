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
        }
    }
}
