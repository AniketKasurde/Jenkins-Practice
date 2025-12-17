pipeline {
  agent any

stages{
 stage('Main Only Stage') {
    when {
        branch 'main'
    }
    steps {
        echo "This runs only on main"
    }
}
}

}

