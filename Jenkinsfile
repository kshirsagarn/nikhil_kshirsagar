pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('Continue ?') {
            steps {
                input message: 'Hello , Should we continue ?', ok: 'Yes please'
            }
        } 
        stage('Script') {
            steps {
                sh 'date'
            }
        }
        
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'Failued'
        }
        success {
            echo 'Success'
        }
    }
}
