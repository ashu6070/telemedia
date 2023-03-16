pipeline {

	agent {
		label {
			label "slave-1"
			customWrokspace "/mnt/proj"
		}
	}
	
	stages {
	
		stage ("stage-1") {
		
			steps { 
			
				sh "sudo docker stop httpd-1"
				sh "sudo docker rm httpd-1"
				sh "sudo docker volume creat index"
				sh "sudo cp /mnt/proj/index.html /var/lib/docker/volumes/index/_data/"
				sh "sudo docker run -itdp 8080:80 -v index:/usr/local/apache2/htdocs --name httpd-2 http"
				
				}
			}
		}




}
