// pipeline {
//     agent any
    
//     stages {
//         stage('Checkout') {
//             steps {
//                 // Checkout your code from version control (e.g., Git)
//                 git 'https://github.com/Airej/gradle-example.git'
//             }
//         }
//         stage('Build') {
//             steps {
//                 // Run Gradle build using gradlew script
//                 sh './gradlew build'
//             }
//         }
//         stage('Test') {
//             steps {
//                 // Run Gradle test task using gradlew script
//                 sh './gradlew test'
//             }
//         }
//     }
// }

pipeline {
    agent any

    stages {
        stage('Print Versions') {
            steps {
                script {
                    // Print Gradle version
                    sh 'gradle --version'
                    
                    // Print Java version
                    sh 'java -version'
                }
            }
        }
    }
}
