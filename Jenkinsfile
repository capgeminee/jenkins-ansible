pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', url: 'https://github.com/shashikanth-t/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
       
      }
    }
 }
}
