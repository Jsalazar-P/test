pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        branch 'main'
      }
      steps {
        ansiblePlaybook(playbook: '/home/omnipro/Documents/ansible/playbooks/test/testing.yml', colorized: true, inventory: '/home/omnipro/Documents/ansible/playbooks/test/hosts', disableHostKeyChecking: true, host_key_checking: False)
      }
    }

  }
  triggers {
    pollSCM('*/5 * * * *')
  }
}
