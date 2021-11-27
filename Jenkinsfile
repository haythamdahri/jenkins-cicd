pipeline {
    agent any

    stages {
        stage('Init') {
            steps {
                echo 'Init Jenkinsfile ...'
            }
        }
        stage('Echo') {
            steps {
                echo 'Running ECHO ...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing ...'
            }
        }
        stage('Ansible Service Check') {
            steps {
                sh 'ansible-playbook /home/haytham/Ansible/AzureMailAdmin.yaml -i /home/haytham/Ansible/inventory_hosts'
            }
        }
    }
}