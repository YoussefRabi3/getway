# la Gateway Spring cloud Gateway avec une Configuration statique du système de routage
## Dans ce cas là il fallait faire 2 configuration une configuration dans application proporties et une autre dans application.yml
 > Configuration d'une application proporties dans la quelle j'ai donné 
   - le nom à le port que je vais utilisé 
   - j'ai donné un nom au micro-service que j'ai appellé gateway-service 
   - et j'ai desactivé l'accès au service EUREKA Avec la commande  spring.cloud.discovery.enabled=true 
  ![image](https://user-images.githubusercontent.com/86606579/207074505-91e32e60-697d-435a-8c04-c187bd4df86c.png)
 - configuration d'une application.yml dans la quelle j'ai donné 
   - id qui r1
   - uri : http://localhost:8081 c'est id de premier web service de client je le donne seulement URL et lui il va chercher l'URL directement 
   - Path = /costumers/** içi je le donne le path ou il se trouve il faut qui soit dans le meme niveau que l'autre path de l'autre web service
 ## je fais la configuration de l'autre web service comme suit 
    - uri : http://localhost:8082 c'est id de deuxieme web service de produit je le donne seulement URL et lui il va chercher l'URL directement 
    - Path = /products/** içi je le donne le path ou il se trouve 
  ![image](https://user-images.githubusercontent.com/86606579/207075715-07b48f43-23cb-4432-9990-a99876186359.png)
# voilà ici comme vous voyez dans le resultat à l'aide de la gatway j'ai pu acceder à les deux micro services au meme temps et c'est ça le role de la gateway c'est connecter deux micro service different
## c'est l'execution de micro-service de client :
   ![image](https://user-images.githubusercontent.com/86606579/207079106-a7183200-6ada-4043-ba79-63136a91d1eb.png)
   ![image](https://user-images.githubusercontent.com/86606579/207079632-5198132e-bf61-474b-b6d5-e5a5bb1f180c.png)
## c'est l'execution de micro-service de produits :
   ![image](https://user-images.githubusercontent.com/86606579/207079284-0946eb1a-1af7-4ef2-823d-e3758266163a.png)
   ![image](https://user-images.githubusercontent.com/86606579/207079483-c1a22a80-6f3e-45af-81e2-2cc3482c60b8.png)
# Voilà le code de deux type de configuration qu'on a une configuration statique et une configuration dynamique :
 ![image](https://user-images.githubusercontent.com/86606579/207089913-f9d223dc-a176-40f9-a30a-8900ac632644.png)





  

   
