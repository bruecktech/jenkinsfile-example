node ('build') {
  stage 'checkout'
  checkout scm

  stage 'build'
  sh 'bin/activator dist'
}
