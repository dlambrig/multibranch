
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
echo "hi"    
    }
  }
        stage('master') {
            when { branch "master" }
            steps { 
               echo "I am a master branch"
            }
        }
        stage('main') {
            when { branch "origin/main" }
            steps { 
               echo "I am a main branch"
            }
        }  
    }
}

