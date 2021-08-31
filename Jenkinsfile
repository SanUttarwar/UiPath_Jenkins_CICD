pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('Build') {
      steps {
        UiPathPack (
          outputPath: "E:\Sandeep\UiPath_Jenkins_CICD_output",
          projectJsonPath: "project.json",
          version: [$class: 'ManualVersionEntry', version: "${MAJOR}.${MINOR}.${env.BUILD_NUMBER}"]
          useOrchestrator: true,
          traceLoggingLevel: "None",
          orchestratorAddress: "https://seludtorch01.tp1.ad1.tetrapak.com/",
          orchestratorTenant: "DEV",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “credentialsId”]
        )
      }
    }
  }
}
