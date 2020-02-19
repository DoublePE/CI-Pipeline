
pipeline {
    agent any
    
stages {
	stage 'Checkout'
		checkout scm        
	stage('Build') {
            steps {
                echo 'Building..'
		bat 'nuget restore TheExampleApp.sln'
		bat 'dotnet build --configuration Release'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
	stage 'Archive'
		archive 'TheExampleApp/bin/Release/**'    }
}
