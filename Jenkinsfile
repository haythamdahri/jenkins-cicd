pipeline {
    agent any

    stages {
        stage('Init') {
            steps {
                echo 'Init Jenkinsfile ...'
            }
        }
        stage('Me') {
            steps {
                sh 'whoami'
            }
        }
        stage('Ansible Service Check') {
            steps {
                // sh 'ansible-playbook /home/haytham/Ansible/AzureMailAdmin.yaml -i /home/haytham/Ansible/inventory_hosts'
                executePlaybook('/home/haytham/Ansible/AzureMailAdmin.yml', '/home/haytham/Ansible/inventory_hosts')
                // sh 'ansible-playbook /home/haytham/Ansible/AzureVMPlaybooks.yml -i /home/haytham/Ansible/inventory_hosts'
                executePlaybook('/home/haytham/Ansible/AzureVMPlaybooks.yml', '/home/haytham/Ansible/inventory_hosts')
            }
        }
    }
}