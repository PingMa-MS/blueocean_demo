pipeline {
  agent any
  parameters {
      string(name: 'Name', defaultValue: 'World', description: 'Name to demo parameters')
  }
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
        echo "Hello, ${params.Name} from Jenkins Blue Ocean!"
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Unit Tests": {
            echo 'Unit Tests Are Awesome!'
            
          },
          "Integration Tests": {
            echo 'Integration Tests Are Awesome!'
            
          },
          "Smoke Tests": {
            echo 'Where There is Smoke there is Fire!!!'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Ship It!'
      }
    }
  }
}
