# WebpageIISRDS
Modifier la page d'accueil de RDS sur IIS


Pour modifier la page de garde de RDS par une interface plus pertinente, aller dans "C:\Windows\Web\RDWeb\Site.xsl"

![image](https://github.com/GleissenJohnson/WebpageIISRDS/assets/115966414/ed28dbc8-a99c-4599-bf8a-757a154d05a5)

Dans ce document, nous pouvons modifier l'apparence du site en choisissant la taille des différents éléments. Les balises <xsl:comment> nous indiquent quel élément est concerné par le code.

Mais l'on peut modifier plus simplement les images en se rendant dans "C:\Windows\Web\RDWeb\Pages\Images"

![image](https://github.com/GleissenJohnson/WebpageIISRDS/assets/115966414/14614ced-81f4-460d-8e15-989a48209979)

Ici, sont stockées les différentes images sur le site, que l'on peut modifier à loisir. Une manière simple de le faire est d'éditer l'image sur paint, et de coller une nouvelle image en conservant les proportions originales.

![image](https://github.com/GleissenJohnson/WebpageIISRDS/assets/115966414/2e391339-f89d-4b80-9ef0-304819f79266)

Dans IIS, il suffit de cliquer sur "restart" et les modifications devraient apparaître.


Pour modifier le texte présent sur la page, il faut se rendre dans "C:\Windows\Web\RDWeb\Pages\fr-FR\RDWAStrings.xml" et modifier les string id qui nous intéressent.

![image](https://github.com/GleissenJohnson/WebpageIISRDS/assets/115966414/2ef15463-e4fd-4b96-9a2d-e42ce9354564)


Pour modifier le titre qui s'affiche sur la page web, il faut utiliser la focntion "Sed-RDWorkspace" du module RemoteDesktop sur powershell de la sorte :

Import-Module RemoteDesktop

Set-RDWorkspace -Name "Applications RDS vivlab.lan" -ConnectionBroker rds.vivlab.lan

![image](https://github.com/GleissenJohnson/WebpageIISRDS/assets/115966414/c3cc7b19-191e-4fbc-b869-9baff26ba054)
