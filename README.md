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

# **What is Application Gateway Ingress Controller?**

L'application Gateway Ingress Controller (AGIC) est une application Kubernetes, ce qui permet aux clients Azure Kubernetes Service (AKS) de tirer parti de la passerelle d'application native d'Azure L7 L7-Balancer pour exposer le logiciel cloud à Internet. AGIC surveille le cluster Kubernetes sur lequel il est hébergé et met à jour en continu une passerelle d'application, afin que les services sélectionnés soient exposés à Internet.

Le contrôleur entrant fonctionne dans son propre pod sur les AK du client. AGIC surveille un sous-ensemble de ressources Kubernetes pour les changements. L'état du cluster AKS est traduit par une configuration spécifique de la passerelle d'application et appliqué à Azure Resource Manager (ARM).
![architecture](https://user-images.githubusercontent.com/108787059/223260871-26e5369d-4240-4830-a8d1-5af109239ba2.png)


# When not to use Azure Application Gateway
Azure Application Gateway isn’t appropriate if you have a web application that doesn’t require load balancing. For example, if you have a web application that only receives a small amount of traffic and the existing infrastructure already competently deals with the existing load, there's no need to deploy a back-end pool of web apps or virtual machines and no need for Application Gateway.

Azure provides other load balancing solutions, including Azure Front Door, Azure Traffic Manager, and Azure Load Balancer. The following list describes the differences between these services:

* **Front Door** is an application delivery network that provides global load balancing and site acceleration service for web applications. It offers Layer 7 capabilities for your application like TLS/SSL offload, path-based routing, fast failover, web application firewall, and caching to improve performance and high-availability of your applications. You'd choose this option in scenarios such load balancing a web app deployed across multiple Azure regions.
* **Traffic Manager **is a DNS-based traffic load balancer that enables you to distribute traffic optimally to services across global Azure regions while providing high availability and responsiveness. Because Traffic Manager is a DNS-based load-balancing service, it load-balances only at the domain level. For that reason, it can't fail over as quickly as Front Door because of common challenges around DNS caching and systems not honoring DNS TTLs.
* **Azure Load Balancer** is a high-performance, ultra low-latency Layer 4 load-balancing service (inbound and outbound) for all UDP and TCP protocols. It's built to handle millions of requests per second while ensuring that your solution is highly available. Azure Load Balancer is zone-redundant, ensuring high availability across availability zones. Azure Load Balancer works within a region rather than globally.
* **Application Gateway **provides application delivery controller (ADC) as a service, offering various Layer 7 load-balancing capabilities. You can use it to optimize web-farm productivity by offloading CPU-intensive TLS/SSL termination to the gateway. Application Gateway works within a region rather than globally.

