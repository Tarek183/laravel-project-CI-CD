pipeline {
 agent any
 stages {
        stage("Build") {
            steps {
                bat 'php --version'
                bat 'composer install'
                bat 'composer --version'
                bat 'copy .env.example .env'
                bat 'php artisan key:generate'
            }
        }
        stage("Unit test") {
            steps {
                bat 'php artisan test'
            }
        }
        stage("Code coverage") {
            steps {
                bat "vendor/bin/phpunit --coverage-html 'reports/coverage'"
            }
        }
       	stage("Sonar metrics") {
            steps {
                script {
                    // this step enable to execute the SonarQube analysis
                    bat "mvn sonar:sonar "
                     }
                }
            } 

  }
}
