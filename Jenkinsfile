pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
            steps {
               echo "Compile Stage@123 "
            }
        }

        stage ('Testing Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
