pipeline {
    agent {label 'imperva'}
    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Hello') {
            steps {
            
              sh '''
              ansible all -i /home/devopsadmin/inventory -m ping -e ansible_ssh_pass=Anil@1234
              '''
            }
        }
    }
}
