#!/usr/bin/env groovy

@Library('piper-library-os-experimental') _

stage ('first stage') {
    node {
        echo "Hello world!"
	deleteDir()
	checkout scm
	sh 'npm config set @sap:registry=https://npm.sap.com'
	mtaBuild script:this, mtaJarLocation:'..', buildTarget:'CF'
    }
}
