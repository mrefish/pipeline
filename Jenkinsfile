pipeline {
  agent any
  parameters {
    string(name: 'ExperimentId', description: 'Provide a unique experiment name')
  }
  stages {
    stage('Create Experiment') {
      steps {
        input 'Please provide an Experiment name'
      }
    }
  }
}
