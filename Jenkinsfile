pipeline {
  agent any
  parameters {
    string(
      name: 'EXPERIMENT_ID',
      description: 'Provide a unique experiment name'
    )
    string(
      name: 'NUMBER_OF_PLATES',
      defaultValue: '1',
      description: 'How many plates are being imaged'
    )
    choice(
      name: 'PLATE_TYPE',
      choices: '96\n384',
      defaultValue: '384',
      description: 'Number of wells for the plate'
    )
    string(
      name: 'SMI_UPLOAD_DIRECTORY',
      defaultValue: '/mnt/nas/Images/UploadWithBarcodes/',
      description: 'The directory on the NAS where the image data can be found'
    )
    choice(
      name: 'NUMBER_OF_CHANNELS',
      choices: '1\n2\n3\n4\n5\n6\n7\n8\n9\n',
      defaultValue: '6',
      description: 'The number of channels being imaged'
    )
    choice(
      name: 'NUMBER_OF_SITES',
      choices: '2x2\n3x3\n4x4\n4x6',
      defaultValue: '2x2',
      description: 'The number of channels being imaged'
    )
    choice(
      name: 'CELL_TYPE',
      choices: 'HUVEC\nA549\nU2OS\nFibroblast',
      defaultValue: 'HUVEC',
      description: 'Cell type present in experiment'
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
