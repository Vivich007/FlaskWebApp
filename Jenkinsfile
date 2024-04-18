pipeline {
    agent any
    stages {
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
