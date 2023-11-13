pipeline {
	agent any;
	tools {nodejs "NodeJs"}

	stages {
		stage('Git') {
			steps {
				git 'https://github.com/vikriramdani8/svgeng-api.git'
			}
		}
		stage('Build') {
			steps {
				sh 'npm install'
			}
		}
		stage('run') {
			steps {
				sh 'pm2 stop index'
				sh 'pm2 start index'
			}
		}
	}
}
