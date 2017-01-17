node( 'buildvm-devops' ) {
	properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [[$class: 'hudson.model.StringParameterDefinition', defaultValue: '', description: 'Some Description', name : 'MY_PARAM'], [$class: 'hudson.model.StringParameterDefinition', defaultValue: '', description: 'Some Description', name: 'MY_PARAM2']]]])

	stage('Output to console') {
		echo "environment: ${env}"
		echo "Should only run manual now"
		sh 'env > env.txt'
		x = readFile('env.txt')
		echo "env: ${x}"
		echo 'Hello, world' 
		sh 'echo "Hello, world -- buildvm!"'
		sh 'echo pwd: $PWD'
		sh 'date'
		sh 'find'
	}
}
