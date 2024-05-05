installo Docker

    curl -ssl https://get.docker.com | bash
  
aggiungo utente a gruppo docker

    sudo usermod -aG docker <user>

inizializzo nodo manager swarm
    
    docker swarm init

inizializzo nodo worker
  
    docker join ... 
  
  se non ho il comando: 
      
    docker swarm join-token worker


creo file bitcoin.conf

  da dir .bitcoin
    
    docker pull python
    docker run -it --rm python bash
	wget https://raw.githubusercontent.com/bitcoin/bitcoin/master/share/rpcauth/rpcauth.py
	python3 rpcauth.py admin password
	exit

  modifico .sample

    docker cp tor:/var/lib/tor/bitcoin_hidden_service/hostname ./hostname

  modifico .sample

creo rete overlay

  	docker network create --driver=overlay --subnet=10.0.1.0/24 --gateway=10.0.1.254 --attachable nodo

creo immagini

avvio container


  
