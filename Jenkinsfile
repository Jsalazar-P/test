pipeline {
  agent any
  stages {
    stage('Deploy') {
      when {
        branch 'main'
      }
      steps {
        sh 'ansible-playbook /home/omnipro/Documents/ansible/playbooks/test/testing.yml -i /home/omnipro/Documents/ansible/playbooks/test/hosts --vv'
      }
    }

  }
  triggers {
    pollSCM('*/5 * * * *')
  }
}
