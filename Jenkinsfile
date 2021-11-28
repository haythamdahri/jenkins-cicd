@Library('shared-libraries') _

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
                executePlaybook('/home/haytham/Ansible/AzureMailAdmin.yaml', '/home/haytham/Ansible/inventory_hosts')
                executePlaybook('/home/haytham/Ansible/AzureVMPlaybooks.yml', '/home/haytham/Ansible/inventory_hosts')
            }
        }
    }
}