pipeline {
    agent {label 'imperva'}
    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Hello') {
            steps {
            
              sh '''
              ansible-playbook -i /home/devopsadmin/inventory first-playbook -e ansible_ssh_pass=Anil@1234
              '''
            }
        }
    }
}
