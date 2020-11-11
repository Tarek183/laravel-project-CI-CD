pipeline {
 agent {
<<<<<<< HEAD
        label "master"
    }
=======
      label "tarek"
 }
>>>>>>> b8bc08232da109c1847202b8906bf86342070817
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
<<<<<<< HEAD
=======
        stage("Code coverage") {
            steps {
                bat "vendor/bin/phpunit --coverage-html 'reports/coverage'"
            }
        }
>>>>>>> b8bc08232da109c1847202b8906bf86342070817
  }
}
