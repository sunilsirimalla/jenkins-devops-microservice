//SCRIPTED PIPELINE
//node {
	// echo "Build"
	// echo "Test"
	// echo "Integration Test"
	// stage('Build') {
	// 	echo "Build"
	// }
	// stage('Test') {
	// 	echo "Test"
	// }
	// stage('Integration Test') {
	// 	echo "Integration Test"
	// }
//}

//DECLARATIVE PIPELINE
pipeline {
	//agent { docker { image 'maven:3.6.3'} }
	agent { docker { image 'node:17.2'} }
	stages {
		stage('Build') {
			steps{
				//sh 'mvn --version'
				// sh 'node --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - env.BUILD_ID"
				echo "JOB_NAME - env.JOB_NAME"
				echo "BUILD_TAG - env.BUILD_TAG"
				echo "BUILD_URL - env.BUILD_URL"
			}
		}
		stage('Test') {
			steps{
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps{
				echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo 'Im awesome, I run always'
		}
		success {
			echo 'Build is successful'
		}
		failure {
			echo 'build failed'
		}
	}
}