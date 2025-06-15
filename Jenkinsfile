pipeline {
    agent any

    stages {
        stage("Restore NuGet Packages") {
            steps {
                echo "📦 Restoring NuGet packages..."
                bat "dotnet restore HouseRentingSystem.sln"
            }
        }

        stage("Build Solution") {
            steps {
                echo "🔨 Building solution..."
                bat "dotnet build HouseRentingSystem.sln --configuration Release"
            }
        }

        stage("Run Tests") {
            steps {
                echo "🧪 Running unit and integration tests..."
                bat "dotnet test tests/HouseRentingSystem.Tests/HouseRentingSystem.Tests.csproj --configuration Release --no-build --logger trx"
            }
        }
    }
}
