pipeline {
  agent {
    kubernetes {
      yaml '''
      spec:
        containers:
        - name: gradle
          image: 'gradle:6.3-jdk14
          command: 'sleep'
          args: '30d'          
        '''
    }
  }
 stages {
    echo 'hi'
 }
}

