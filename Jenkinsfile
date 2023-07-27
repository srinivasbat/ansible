pipeline {
     agent { label 'ansible-master' }

    stages {
        stage('Checkout') {
            steps {
                // This step will check out the code from your Git repository
                checkout scm
            }
        }

        stage('Ansible Deployment') {
            steps {
                // This step will run the Ansible playbook using the 'hosts' file from the Jenkins workspace
                script {
                    sh 'ansible-playbook -i /root/workspace/ansible/hosts /root/workspace/ansible/playbook.yaml'
                }
            }
        }
    }
}
