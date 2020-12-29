pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        branch 'main'
      }
      steps {
        ansiblePlaybook(playbook: '/home/omnipro/Documents/ansible/playbooks/test/testing.yml', colorized: true, inventory: '/home/omnipro/Documents/ansible/playbooks/test/hosts', disableHostKeyChecking: true)
        sh 'mkdir -p /home/jsalazar/test/prueba'
      }
    }

  }
  triggers {
    pollSCM('*/5 * * * *')
  }
}
