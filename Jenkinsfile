pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        branch 'main'
      }
      steps {
       # ansiblePlaybook(playbook: '/home/omnipro/Documents/ansible/playbooks/test/testing.yml', colorized: true, inventory: '/home/omnipro/Documents/ansible/playbooks/test/hosts', disableHostKeyChecking: true, --vvv)
        sh 'ansible-playbook /home/omnipro/Documents/ansible/playbooks/test/testing.yml -i /home/omnipro/Documents/ansible/playbooks/test/hosts --vv'
      }
    }

  }
  triggers {
    pollSCM('*/5 * * * *')
  }
}
