pipeline {
    agent {label 'imperva'}
    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
       stage('checkout'){
        git branch: 'main', url: 'https://github.com/krithika1722/anil.git'
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
