# Born2BeRoot
## 42 project - Administration system

Afficher le nom de la machine:
```hostname```

Savoir quels utilisateurs sont actuellement connectés:
```who```

Afficher le nom de l'utilisateur actuel:
```whoami```

Changer le mot de passe de l’utilisateur actuel: 
```passwd```

Installer “sudo”:
```apt-get install sudo```

Configurer “sudo”:
```sudo visudo```

Définir un nouveau “hostname” pour la machine:
```sudo hostnamectl set-hostname [new_hostname]```

Connexion au serveur SSH:
```ssh [user]@localhost -p [port]```

Configuration du serveur SSH:
```nano etc/ssh/sshd_config```

Voir les groupes auquels appartient l'utilisateur:
```groups [user_name]```

Ajouter un utilisateur:
```sudo adduser [user_name]```

Créer un nouveau group:
```sudo addgroup [group_name]```

Ajouter un utilisateur a un groupe:
```sudo adduser [user_name] [group_name]```

Voir les utilisateurs appartenant au groupe souhaité:
```cat /etc/group | grep [group_name]```

Changer le chemin de journalisation des logs de “sudo” pour les inputs seulement:
```
sudo visudo
	Add lines:
	> Defaults logfile="/var/log/sudo/log_command"
	> Defaults iolog_dir="/var/log/sudo/"
	> Defaults log_input,log_output
sudo systemctl restart rsyslog
```

Politique de mot de passe fort:
```
sudo apt-get install libpam-pwquality (ajoute des règles de sécurité)
nano /etc/pam.d/common-password
```

Configurer date d’expiration mot de passe:
```sudo nano /etc/login.defs```

Pare-feu UFW:
```
sudo service ufw [status / start / stop / restart]
sudo ufw status
```

Ajouter une règle UFW: ```sudo ufw allow [port]```

Supprimer une règle UFW: ```sudo ufw delete [line_of_the_port_in_ufw_status]```

Cron automatisation:
```
sudo apt-get install cron
sudo /etc/crontab
	> Ajout de regles
sudo service cron (status / start / stop / restart)
```

##### *Nano >>>>>>>>> Vim*
