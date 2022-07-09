# PictsManager

![Logo](https://cdn.discordapp.com/attachments/959024336075898903/992883530013102181/telechargement.png)

## Qu'est-ce que le PictsManager ?

<p>
Le PictsManager est une application mobile de partage d'images compressées.

L'utilisateur se connecte, depuis l'appli' mobile.
Une fois connecté, il peut prendre avec la caméra de son téléphone une photo, qu'il va ensuite comprésser à sa guise avant de l'uploader.
Cette dite photo peut ensuite être visionnée, placée dans un album ou même partagée à un autre utilisateur de l'application.
</p>



## Lancer le projet

<p>
Pour lancer le projet il vous utiliser la commande suivante :

```
docker-compose up --build
```

Pour télécharger docker et docker-compose vous pouvez utiliser le lien suivant:
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-fr
</p>

![Gif](https://cdn.discordapp.com/attachments/959024608688885791/994694932344357114/ezgif-3-37f5501a5c.gif)

## L'Apk

<p>
L'APK généré par le docker-compose pointe normalement sur un serveur host (production). Pour des raisons de sécurité, l'IP a été changée. Vous pouvez toujours passer par le docker-compose pour générer l'APK, cependant il n'arrive pas à se connecter en production. Si vous souhaitez vraiment tester en production, n'hésitez pas à me contacter.
Les commandes pour générer l'APK localement (sans passer par Docker) sont:

```
cd mobile && npm run build:android
```

L'APK généré se retrouvera au path suivant :

```
mobile/android/app/build/outputs/apk/release/app-release.apk
```

Sinon, vous pouvez toujours faire tourner l'appli' en local (ce qui fonctionnera) :

```
cd mobile && npm run android
```

N'oubliez pas d'installer les packages npm (npm i), de connecter un téléphone à votre ordinateur et de le configurer pour que le Debug USB soit activé.

Enfin, pour que votre appli' mobile arrive à se connecter à vos serveurs en local, il faut que votre appareil mobile soit connecté au même réseau que votre machine. De plus, il faut aller rajouter votre adresse IP au fichier .env.local pour le compléter avec votre IP. (./mobile/.env.mobile)

</p>

## Technologies utilisées

Back: ExpressJS

Mobile: React Native

La maquette Figma du projet est disponible à [ce lien](https://www.figma.com/file/ZDPlISu98vP9mffcNX090x/PictsManager-App?node-id=224%3A1872).