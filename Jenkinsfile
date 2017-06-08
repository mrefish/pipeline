pipeline {
  agent any
  parameters {
    string(name: 'EXPERIMENT_ID', description: 'Provide a unique experiment name')
  }
  stages {
    stage('Create Experiment') {
      steps {
        echo "Starting ${params.EXPERIMENT_ID}"
      }
    }
  }
}
