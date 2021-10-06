pipeline {
  agent {
    kubernetes {
      yaml '''
      spec:
        containers:
        - name: gradle
          image: gradle:6.3-jdk14     
'''
    }
  }
stages {
  stage('first') {
    steps {
def branch_nem = scm.branches[0].name
if (branch_nem.contains("*/")) {
    branch_nem = branch_nem.split("\\*/")[1]
    }
echo branch_nem      
    }
  }
        stage('master') {
            when { branch "master" }
            steps { 
               echo "I am a master branch"
            }
        }
        stage('main') {
            when { branch "main" }
            steps { 
               echo "I am a main branch"
            }
        }  
    }
}

