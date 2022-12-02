pipeline {
    agent any
    stages {
	
	stage('Non-Parallel Stage') {
	    
        steps {
                echo 'This stage will be executed first'
                }
        }

	
        stage('Run Tests') {
            parallel {
                stage('Test On Windows') {
                    agent {
                        label "windows_node"
                    }
                    steps {
                        echo "Task1 on Agent"
                    }
                                   }
                
                }
            }
        }
    }
}
