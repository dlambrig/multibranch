podTemplate(containers: [
    containerTemplate(
        name: 'maven', 
        image: 'maven:3.8.1-jdk-8', 
        command: 'sleep', 
        args: '30d'
        ),
  ],
  volumes: [
  persistentVolumeClaim(
      mountPath: '/root/.m2/repository', 
      claimName: 'jenkins-pv-claim', 
      readOnly: false
      )
  ]) {

    node(POD_LABEL) {
       stage('Run pipeline against a gradle project') {
            git 'https://github.com/dlambrig/Continuous-Delivery-with-Docker-and-Jenkins-Second-Edition.git'
            container('gradle') {
   
                stage('Build a gradle project') {
                    sh '''
                    cd Chapter08/sample1
                    chmod +x gradlew
                    '''
                    }
            }
        }

    }
  }
