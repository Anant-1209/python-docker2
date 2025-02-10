pipeline {

    agent { label 'agent-anant1' }
 
    stages {

        stage('Clone Repository') {

            steps {

                // Remove any existing directory before cloning the repo
                sh 'rm -rf python-docker2 || true'

                // Clone the repository
                sh 'git clone -b main https://github.com/Anant-1209/python-docker2.git'

                echo "Cloned..."

            }

        }

        stage('Run') {

            steps {
                // Use a single shell step to navigate into the directory and run the commands
                sh '''
                    cd python-docker2
                    ls -l
                    python3 python.py
                    
                    echo "Completed"
                '''

            }

        }

    }

}
