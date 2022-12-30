node("linux"){
    stage("Git checkout"){
        git credentialsId: 'f59aef6e-8d62-4533-bf96-fe5977309a56', url: 'git@github.com:AleksTurbo/example-playbook.git'
    }
    stage("Run playbook"){
        if (secret_check){
            sh 'ansible-playbook site.yml -i inventory/prod.yml'
        }
        else{
            echo 'need more action'
        }
        
    }
}