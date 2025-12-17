pipeline {
  agent any

  
  stages {
  
    stage('always run'){

	steps { 
          echo "this runs on all branches"
                  
}

}

  stage('main only'){
    
     when {

	branch 'main'

}

     steps {

        echo "this runs only on main branch"

}


}

}


}
