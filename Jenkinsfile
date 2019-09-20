pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('deploy'){
            parallel {               
                    stage('deploy1') {
                        input {
                                message "Are you ready to deploy?"
                                ok "yes please deploy"
                        }
                        steps{
                              sh 'echo deploy1'
                        }
                    }                
                    stage('deploy2') {
                         input {
                                message "Are you ready to deploy?"
                                ok "yes please deploy"
                        }
                        steps {
                              sh 'echo deploy2'  
                    }
                }
            }
        }
    }
}
