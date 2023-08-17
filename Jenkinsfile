pipeline{
    agent any
    stages{
        stage('SCM checkout')
        {
          
            steps{
                git branch: 'main', url: 'https://github.com/prakrishna2004/myansible.git'
            }
        }
        stage('Ansible playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'ansible1', disableHostKeyChecking: true, installation: 'myansible', inventory: 'playbook_dev.inv', playbook: 'playbook.yml'
            }
        }
    }
}
