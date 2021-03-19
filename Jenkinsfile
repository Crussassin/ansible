pipeline {
    agent any 
    stages {
        stage('repo'){
            steps{
                git branch: 'master', credentialsId: '9a07c6ec-80d9-43f2-923e-572c2065bc24', url: 'https://github.com/Crussassin/ansible'
            }
        }
        stage('playbook'){
            steps{
                
                ansiblePlaybook credentialsId: '9a07c6ec-80d9-43f2-923e-572c2065bc24', disableHostKeyChecking: true, installation: 'ansible_slave', inventory: 'exam_2', playbook: 'roles.yml'
            }
        }
		
    }
}
