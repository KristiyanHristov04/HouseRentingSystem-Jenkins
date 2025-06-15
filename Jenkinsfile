pipeline {
    agent any

    stages {
        stage("Restore NuGet Packages") {
            steps {
                echo "📦 Restoring NuGet packages..."
                bat "dotnet restore"
            }
        }

        stage("Build Solution") {
            steps {
                echo "🔨 Building solution..."
                bat "dotnet build"
            }
        }

        stage("Run Tests") {
            steps {
                echo "🧪 Running unit and integration tests..."
                bat "dotnet test"
            }
        }
    }
}
