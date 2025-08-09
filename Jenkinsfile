pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo '📥 Clonage du repo...'
                checkout scm
            }
        }

        stage('Run Python App') {
            steps {
                echo '🚀 Lancement de app.py'
                // Pour Windows
                bat 'python app.py'
                // Si tu es sur Linux, utilise :
                // sh 'python3 app.py'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline terminé avec succès.'
        }
        failure {
            echo '❌ Pipeline échoué à cause d’une erreur réelle dans le code.'
        }
    }
}
