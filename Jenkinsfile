pipeline {
    agent any
    tools {
        gradle 'GRADLE_HOME_7.3'
        //jave '14.1'
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from version control (e.g., Git)
                git 'https://github.com/Airej/gradle-example.git'
            }
        }
        stage('Build') {
            steps {
                // Run Gradle build using gradlew script
                sh './gradlew build'
            }
        }
        stage('Test') {
            steps {
                // Run Gradle test task using gradlew script
                sh './gradlew test'
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

