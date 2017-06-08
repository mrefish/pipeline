pipeline {
  agent any
  parameters {
    string(
      name: 'EXPERIMENT_ID', 
      description: 'Provide a unique experiment name'
    ),
    string(
      name: 'NUMBER_OF_PLATES', 
      description: 'How many plates are being imaged'
    ),
    choice(
      name: 'PLATE_TYPE', 
      choices: '96\n384', 
      description: 'Number of wells for the plate'
    ),
    choice(
      name: 'CELL_TYPE',
      choices: 'HUVEC\nA549\nU2OS\nFibroblast', 
      description: 'Cell type present in experiment'
    ),
    string(
      name: 'SMI_UPLOAD_DIRECTORY', 
      description: 'The directory on the NAS to upload images from (if not /UploadWithBarcodes/)'
    )
  }
  stages {
    stage('Create Experiment') {
      steps {
        echo "Starting ${params.EXPERIMENT_ID}"
      }
    }
  }
}
