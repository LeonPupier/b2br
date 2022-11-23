# Born2BeRoot
## 42 project - Administration system

Afficher le nom de la machine:
```hostname```

Définir un nouveau “hostname” pour la machine:
```hostname set-hostname [new_hostname]```

Savoir quel utilisateur est actuellement connecté:
```whoami```

Connexion au serveur SSH:
```ssh [user]@localhost -p 4242```

Configuration du serveur SSH:
```nano etc/ssh/sshd_config```

Voir les groupes présents sur le pc:
```groups```

Créer un nouveau group:
```sudo groupadd [new_name_group]```

Ajouter un utilisateur a un groupe:
```sudo user mod -a -G [name_group] [name_user]```

Voir les utilisateurs appartenant au groupe souhaité:
```cat /etc/group | grep [group_name]```

Installer “sudo”:
```apt-get install sudo```

Configurer “sudo”:
```sudo visudo```

Changer le chemin de journalisation des logs de “sudo”:
```
sudo visudo
	> add line at the end: “Defaults syslog=local1”
sudo nano /etc/rsyslog.conf
	> add line number 61: “local1.*	/var/log/sudo/“
sudo systemctl restart rsyslog
```

Ajouter un utilisateur:
```sudo adduser [new_user_name]```

Politique de mot de passe fort:
```
sudo apt-get install libpam-pwquality (ajoute des règles de sécurité)
nano /etc/pam.d/common_password
```

Configurer date d’expiration mot de passe:
```sudo nano /etc/login.defs```

Pare-feu UFW:
```
sudo service ufw (status / start / stop / restart)
sudo ufw status
```

Cron automatisation:
```
sudo apt-get install cron
crontab -e (avec l’user “root” actif)
sudo service cron (status / start / stop / restart)
```

Changer le mot de passe de l’utilisateur actuel:
```passwd```
