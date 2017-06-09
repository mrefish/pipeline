pipeline {
  agent any
  stages {
    stage('Create barcodes') {
      steps {
        script {
          env['BARCODES'] = sh(script: """env LC_CTYPE=C tr -dc "a-zA-Z0-9" < /dev/urandom | head -c 6""", returnStdout: true).trim()
        }
        
        echo '"Starting ${params.EXPERIMENT_ID}"'
        echo '"Barcodes:  ${env.BARCODES}"'
      }
    }
  }
  parameters {
    string(name: 'EXPERIMENT_ID', description: 'Provide a unique experiment name')
    string(name: 'NUMBER_OF_PLATES', defaultValue: '1', description: 'How many plates are being imaged')
    choice(name: 'PLATE_TYPE', choices: '''96
384''', description: 'Number of wells for the plate')
    string(name: 'SMI_UPLOAD_DIRECTORY', defaultValue: '/mnt/nas/Images/UploadWithBarcodes/', description: 'The directory on the NAS where the image data can be found')
    choice(name: 'NUMBER_OF_CHANNELS', choices: '''1
2
3
4
5
6
7
8
9
''', description: 'The number of channels being imaged')
    choice(name: 'NUMBER_OF_SITES', choices: '''2x2
3x3
4x4
4x6''', description: 'The number of channels being imaged')
    choice(name: 'CELL_TYPE', choices: '''HUVEC
A549
U2OS
Fibroblast''', description: 'Cell type present in experiment')
  }
}