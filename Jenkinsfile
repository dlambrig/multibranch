pipeline {
    podTemplate(containers: [
    containerTemplate(
        name: 'gradle', 
        image: 'gradle:6.3-jdk14', 
        command: 'sleep', 
        args: '30d'
        ),
  ]) {
    
    agent(POD_LABEL) {
        echo 'hi'
    }
}
}
