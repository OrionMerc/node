#!groovy

pipeline {
  agent any
  tools {nodejs "NodeGrupoOST"}
  stages {
     stage('Docker Build') {
            agent any
            steps {
                sh 'npm install'
            }
        } 
    stage ('build'){
      steps{
        sh 'npm build /var/lib/jenkins/workspace/atividade_grupo_orion_surya_thiago@2/tools/doc/package.json'
      }
    }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }

}
