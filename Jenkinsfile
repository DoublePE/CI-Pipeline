node {
	stage 'Checkout'
	checkout scm

	stage 'Build'
	bat 'nuget restore TheExampleApp.sln'
	bat 'dotnet build'

	stage 'Archive'
	archive 'ProjectName/bin/Release/**'

}

