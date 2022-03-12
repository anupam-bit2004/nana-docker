pipeline {
    agent any

    stages {
        stage('Build') {
           when {
             expression {
                BRANCH_NAME == 'master' 
             }
           } 
            steps {
                echo 'Building the app..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the app..'
                echo "executing pipeline for branch $BRANCH_NAME"
            }
        }
        stage('Deploy') {
            when {
             expression {
                BRANCH_NAME == 'master' 
             }
           } 
            steps {
                echo 'Deploying the app....'
            }
        }
    }
}
