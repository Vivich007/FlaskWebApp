pipeline {
    agent any
    stages {
        stage('Git checkout') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/Vivich007/FlaskWebApp.git'
            }
        }
        
        stage('Install Python and Flask') {
            steps {
                ansiblePlaybook(
                    playbook: 'install_python.yml',
                    inventory: 'FlaskHosts.ini',
                    credentialsId: 'Ansible-Project'
                )
            }
        }
    }
}
