podTemplate(containers: [
    containerTemplate(
        name: 'gradle', 
        image: 'gradle:6.3-jdk14', 
        command: 'sleep', 
        args: '30d'
        ),
  ]) {
    node(POD_LABEL) {
        stage('Run pipeline against a gradle project') {
            if (env.BRANCH_NAME == 'master') {
                echo 'nope'
            } else {
                echo env.BRANCH_NAME
                git 'https://github.com/dlambrig/Continuous-Delivery-with-Docker-and-Jenkins-Second-Edition.git'
                container('gradle') {
   
                    stage('Build a gradle project') {
                        step {
                            sh '''
                            cd Chapter08/sample1
                            chmod +x gradlew
                            '''
                        }        
                    }
                }
            }
        }
    }
}
