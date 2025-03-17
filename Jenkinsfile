pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN3.9.9"
    }

    stages {
        stage('scm') {
            steps {
	    // Get some code from a GitHub repository
                git 'https://github.com/ananyachowhan/TomcatMavenApp'
	    }
	}
	stage('Build') {
            steps {
            	// To run Maven on a Windows agent, use
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }

    }
}
