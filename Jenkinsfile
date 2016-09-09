node ('build') {
  stage 'checkout'
  checkout scm

  stage 'build'
  wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'XTerm']) {
    sh 'bin/activator dist'
  }
  sh "aws s3 cp target/universal/play-scala-1.0-SNAPSHOT.zip s3://as24-artifacts-eu-west-1/jenkinsfile-example/${env.BUILD_NUMBER}/"
}
