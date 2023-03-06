# Meetup-Azure-Microsoft-365-Community-Azure-Application-Gateway

Azure Application Gateway est un service Azure qui traite le trafic vers des applications Web qui sont desservies par un pool de serveurs Web. Ce traitement inclut le trafic HTTP équilibrant le chargement, inspectant le trafic à l'aide d'un pare-feu d'application Web, cryptant le trafic entre les utilisateurs et une passerelle d'application et cryptant le trafic entre les serveurs d'application et une passerelle d'application.

* Détecter si l'un des serveurs sur site est devenu indisponible afin que le trafic ne soit plus dirigé vers cela 
* Fonctionnalité de terminaison TLS pour réduire la quantité de capacité CPU consommée par les opérations de cryptage et de décryptage
* Affinité de session pour s'assurer qu'un client utilisant une session d'une application Web est géré par le même serveur Web dans le pool
* Filtrage de sécurité du trafic malveillant tel que l'injection SQL et les attaques de scripts de site croisé


# ** Qu'est-ce que la passerelle d'application Azure?**
Azure Application Gateway gère les demandes que les applications clients envoient aux applications Web hébergées sur un pool de serveurs Web. Le pool de serveurs Web peut être des machines virtuelles Azure, des ensembles d'échelles de machines virtuels Azure, un service d'application Azure et même des serveurs sur site.

Application Gateway fournit des fonctionnalités telles que l'équilibrage de charge HTTP, le pare-feu d'application Web et la prise en charge du chiffrement TLS / SSL du trafic entre les utilisateurs et une passerelle d'application et entre les serveurs d'application et une passerelle d'application.

> here image application-gateway-topology
> ![application-gateway-topology](https://user-images.githubusercontent.com/108787059/223244209-052189a8-7515-4976-b67e-1fb3ef752408.png)

> 

Azure Application Gateway comprend les fonctionnalités suivantes:

* Prise en charge des protocoles HTTP, HTTPS, HTTP / 2 et WebSocket
* Un pare-feu d'application Web pour protéger contre les vulnérabilités d'application Web
* Cryptage de demande de bout en bout
* Automatiquement pour ajuster dynamiquement la capacité à mesure que votre charge de trafic Web change
* Drainage de connexion permettant la suppression gracieuse des membres du pool back-end lors des mises à jour de service prévues
