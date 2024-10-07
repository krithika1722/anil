pipeline {
    agent {label 'imperva'}
    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
       stage('checkout') {
        steps {
           git branch: '${branch}', url: "${url}"
        }
       }
        stage('ansible') {
            steps {
            
              sh '''
              ansible-playbook -i /home/devopsadmin/inventory first-playbook.yml -e ansible_ssh_pass=Anil@1234
              '''
            }
        }
    }
}
