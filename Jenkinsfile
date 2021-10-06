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
                branchName = sh(label: 'getBranchName', returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
                println branchName
        }
    }
}
