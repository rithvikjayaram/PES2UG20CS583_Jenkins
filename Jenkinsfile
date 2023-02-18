pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o pes2ug20cs583-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './pes2ug20cs583-1'
        }
    }
    
   
}

post {
    always {
        script {
            if (currentBuild.result == "FAILURE") {
                echo "Pipeline failed"
            }
        }
    }
}
}
