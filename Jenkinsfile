pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        branch 'staging'
      }
      steps {
        ansiblePlaybook(playbook: '/home/omnipro/Documents/ansible/playbooks/test/staging-test.yml', colorized: true, inventory: '/home/omnipro/Documents/ansible/playbooks/test/hosts', disableHostKeyChecking: true)
      }
    }

  }
  triggers {
    pollSCM('*/5 * * * *')
  }
}
