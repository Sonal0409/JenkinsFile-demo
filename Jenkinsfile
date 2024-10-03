pipeline{
    agent {
        label 'linux_node'
    }
    parameters{
        string(name: 'PERSON',defaultValue: 'Mr.Jenkins',description: 'Give name of the Person ')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage('use Parameters'){
            steps{
                echo "Hello ${params.PERSON}"
                
                echo "Hello ${params.BIOGRAPHY}"
                
                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
}
