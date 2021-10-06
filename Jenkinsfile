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
BRANCH_NAME = "${GIT_BRANCH.split('/').size() > 1 ? GIT_BRANCH.split('/')[1..-1].join('/') : GIT_BRANCH}"

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

