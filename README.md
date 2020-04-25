# angular-9-jwt-authentication-example

Angular 9 - JWT Authentication Example with the Angular CLI -- 

#Coquille Angular qui se co a https://api02.ddadev.fr/ qui est un container API-mongo-express-jwt et des services mails/notifs/slack ok

To see a demo and further details go to https://jasonwatmore.com/post/2020/04/19/angular-9-jwt-authentication-example-tutorial


#pr lancer une premiere fois le container pr faire mes tests sur un container random
docker run -it sandbox_angular9_app_angular_sandbox bash

#trouver l adresse ip
docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' compassionate_edison

####FAIL : 
ng serve --port 80 --host 172.18.0.12 --ssl=true ##SSL HS ET IP LOCALE PAS DETECTEE
ng serve --port 80 --host 51.91.109.234 HS CAR PORT 80 DEJA USE PAR NGINX
#SOLUTION:
"start": "ng serve --port 4200 --host 0.0.0.0",


###une fois mes modifs faites, je fais une image de mon result et je le push sur le hub
docker commit node-angular9-sandbox ddaconseil/angular-9-dev-machine:first
docker push ddaconseil/angular-9-dev-machine:first