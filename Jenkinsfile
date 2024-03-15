pipeline {
    agent any
    tools {
        gradle 'GRADLE_HOME_7.3'
        jdk 'JDK-my'
    }
    stages {
        stage('Checking versions') {
            steps {
                sh 'java -version'
                sh 'gradle -version'
            }
        }

        stage('Test') {
            steps {
                // Run Gradle test task using gradlew script
                sh './gradlew test'
            }
        }

        stage('Build') {
            steps {
                // Run Gradle build using gradlew script
                sh './gradlew build'
                sh './gradlew shadowJar'
                sh 'java -jar build/libs/gradle-example-all.jar'
            }
        }

    }
}

// pipeline {
//     agent any

//     stages {
//         stage('Print Versions') {
//             steps {
//                 script {
//                     sh "/var/lib/jenkins/.gradle/wrapper/dists/gradle-6.4.1-all/13imxtezgn9nwzqt8rgtkunh1/gradle-6.4.1/bin/gradle --version"
                    
//                     // Print Java version
//                     sh 'java -version'
//                 }
//             }
//         }
//     }
// }
