pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Ensure to use the right credentials ID
                    def scmVars = checkout([
                        $class: 'GitSCM',
                        branches: [[name: 'main']],
                        userRemoteConfigs: [[
                            url: 'https://github.com/Basant-mahmoud/task_cloud.git',
                            credentialsId: 'your-credentials-id'
                        ]]
                    ])
                }
            }
        }
        stage('Print Hello World') {
            steps {
                // Print Hello World
                echo 'Hello World'
            }
        }
    }
}
