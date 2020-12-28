pipeline {
  agent any
  triggers {
    pollSCM('*/5 * * * *')
    }
  stages {
    stage('Deploy') {
      when {
        branch 'main'
      }
      steps {
        ansiblePlaybook(playbook: '/home/omnipro/Documents/ansible/playbooks/test/testing.yml', colorized: true, inventory: '/home/omnipro/Documents/ansible/playbooks/test/hosts')
      }
    }
  }
}
