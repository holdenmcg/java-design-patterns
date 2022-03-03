pipeline {
  agent any
  stages {
    stage('Semgrep-Scan') {
        steps {
            sh 'ls -la'
            sh '''docker pull returntocorp/semgrep-agent:v1 && \
    docker run -v "$(pwd):$(pwd)" --workdir $(pwd) \
    returntocorp/semgrep-agent:v1 semgrep-agent \
    --publish-token \
    eacdb937b34b3b6ee932f6224d3af01f3649f75c5f78682320a4fdddc2addebe'''
        }
    }
  }
}