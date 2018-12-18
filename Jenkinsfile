#!/usr/bin/env groovy

@Library('piper-library-os-experimental') _

stage ('first stage') {
    node {
        echo "Hello world!"
	deleteDir
	checkout scm
	mtaBuild script:this, mtaJarLocation:'..', buildTarget:'CF'
    }
}
