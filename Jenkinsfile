
pipeline {
    agent any
    
stages {
	stage ('Checkout'){
		steps{
                echo 'Checkout..'	
		checkout scm
	    }
	}
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
	stage ('Archive'){
		steps{
		archive 'TheExampleApp/bin/Release/**'
	        }
        }
}
