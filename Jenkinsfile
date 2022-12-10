pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        java --version
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/amorphous4u/jenkins-java-job.git'

                // Run Maven on a Unix agent.
                sh "hostname"

                // To run Maven on a Windows agent, use
                //bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    //junit '**/target/surefire-reports/TEST-*.xml'
                    // archiveArtifacts 'target/*.jar'
                    echo "created target.jar"
                }
            }
        }
    }
}
