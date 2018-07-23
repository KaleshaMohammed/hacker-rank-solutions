#!/usr/bin/env groovy
/**
 * It is testing jenkins file
*/
def branch = "master"

echo "print ${branch}"

echo "build URL : ${BUILD_URL}"
echo "build ID : ${BUILD_ID}"

echo "build number : ${env.BUILD_NUMBER}"
echo "JOB NAME : ${env.JOB_NAME}"
try {
  node {
      stage 'Build'
        echo "Build stage started "
        echo "Build 2nd line"
      stage 'Test' 
        echo "Test stage"
  }
} catch(all) {
  echo "exception : ${all}"
} finally {
  echo "finally executed"
}
