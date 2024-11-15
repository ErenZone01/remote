# Mise à jour des paquets
sudo apt update

# Installation du serveur SSH
sudo apt install openssh-server

# Modification du port SSH
sudo nano /etc/ssh/sshd_config
# Changer `Port 22` par `Port 2000`
sudo systemctl restart ssh

# Vérifier et configurer ufw si nécessaire
sudo ufw status
sudo ufw allow 2000/tcp
sudo ufw reload

# Reconfigurer la machine vituelle 
changer le port en mettant le meme que celui qui était dans ta modification du port ssh 'Port 2000'

# Connexion SSH depuis la machine hôte
ssh -p 2222 user@localhost
