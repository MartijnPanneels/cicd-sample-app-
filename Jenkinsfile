node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop samplerunning'
            sh 'docker rm samplerunning'
        }
    }
    stage('Build') {
        build 'BuildSampleApp'  # Ensure this matches your actual build job
    }
    stage('Results') {
        build 'TestSampleApp'  # Ensure this matches your actual test job
    }
}
