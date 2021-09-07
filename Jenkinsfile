pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                build job: "dummy-job", parameters: [string(name: 'upstreamProjectName', value: "${JOB_NAME}"), string(name: 'upstreamBranch', value: "${GIT_BRANCH}"), string(name: 'upstreamRunId', value: "${BUILD_ID}")]
            }
        }
    }
}
