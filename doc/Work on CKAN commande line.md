# Ensemble des commandes fréquement utilisés



activer le virtual env
```
. /usr/lib/ckan/default/bin/activate
```

Connection psql
```
sudo -u postgres psql -d ckan_default
```



Arreter nginx apache psql
```
sudo /etc/init.d/nginx stop
sudo /etc/init.d/apache2 stop
sudo /etc/init.d/postgresql stop
```

redemarer apache jetty nginx  psql
```
sudo /etc/init.d/apache2 restart

sudo /etc/init.d/jetty8 restart

sudo /etc/init.d/nginx restart
sudo /etc/init.d/postgresql restart
```




Voir les logs 
```
sudo nano /var/log/apache2/ckan_default.custom.log
sudo nano /var/log/apache2/ckan_default.error.log
sudo nano /var/log/postgresql/postgresql-9.4-main.log
```

# gestion des droits sur les fichiers

ajouter des droits de lecture et d'écriture aux membres du groupe propriétaire sur un dossier et se fils
```
sudo chmod -R g+wr [file]
```
changement de proprietaire
```
chwon
```

ajouter un utilisateur (cartong) existant à un groupe (root)
```
sudo usermod -a -G root cartong
sudo usermod -a -G adm cartong
sudo usermod -a -G jetty cartong
```
verifier les groupes d'un user (cartong)
```
groups cartong
```

check pgis tables
```
sudo -u postgres psql -d ckan_default
\d package_extent
```