 pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'git_id', url: 'https://github.com/Shibaprasaddalai/jenkins-ansible.git'
       }
 }
  stage('Execute Ansible'){
   steps{
      ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, inventory: 'dhost.inv', playbook: 'apache.yml'  
      }
    }
}
}
