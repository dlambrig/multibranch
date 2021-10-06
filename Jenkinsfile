
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
echo env.GIT_BRANCH
    }
  }
        stage('master') {
            when { branch "master" }
            steps { 
               echo "I am a master branch"
            }
        }
        stage('orgin/main') {
            when { branch "origin/main" }
            steps { 
               echo "I am a main branch"
            }
        }  
    }
}

