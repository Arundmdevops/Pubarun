pipeline {
	agent any
	tools{
		maven = 'MAVEN'
	}
		stages {
			stage("git") {
				steps{
				 git branch: 'main', url: 'https://github.com/Arundmdevops/Pubarun.git'
				}
			}
			stage("maven build") {
                                steps{
					maven_invoker invokerBuildDir: 'target/it', reportsFilenamePattern: 'target/invoker-reports/BUILD*.xml'
					sh "mvn clean install"
                                }
                        }

		}
	}
