
 pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
      git branch: 'main', credentialsId: 'naveen', url: 'https://github.com/uday2312/jenkins-ansible.git'
       }
 }

 stage('Execute Ansible'){
  steps{   
      ansiblePlaybook credentialsId: 'pipeline', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
      }
 }
    }

}
