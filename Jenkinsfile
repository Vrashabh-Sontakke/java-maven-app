pipeline {
    agent any
    paramenters {
        choice(name: 'VERSION', choices: ['1.0', '2.0', '3.0'], description: 'Version to deploy')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'execute tests')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building version ${params.VERSION}"
            }
        }
        stage('Test') {
            when {
                expression { params.executeTests }
            }
            steps {
                echo "Testing version ${params.VERSION}"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying version ${params.VERSION}"
            }
        }
    }

}