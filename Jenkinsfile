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
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
}

