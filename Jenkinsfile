pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('test'){
            parallel {               
                    stage('deploy1') {
                        sh 'echo deplo1'
                    }                
                stage('deploy2') {
                    sh 'echo deploy2'                   
                }
            }
        }
    }
}
