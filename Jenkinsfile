
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
echo env.GIT_LOCAL_BRANCH 
    }
  }
        stage('feature') {
            when { branch "feature" }
            steps { 
               echo "I am a feature branch"
            }
        }
        stage('main') {
            when { branch "*main*" }
            steps { 
               echo "I am a main branch"
            }
        }
    }
}

