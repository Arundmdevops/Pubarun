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
                                 sh "mvn clean install"
				 maven_invoker invokerBuildDir: 'target/it', reportsFilenamePattern: 'target/invoker-reports/BUILD*.xml'
                                }
                        }

		}
	}
