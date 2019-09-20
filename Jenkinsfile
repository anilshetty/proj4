pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('deploy'){
            input {
                                message "Are you ready to deploy?"
                                ok "yes please deploy"
                        }
            parallel {               
                    stage('deploy1') {
                        
                        steps{
                              sh 'echo deploy1'
                        }
                    }                
                    stage('deploy2') {
                         
                        steps {
                              sh 'echo deploy2'  
                    }
                }
            }
        }
    }
}
