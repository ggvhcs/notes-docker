# --- *** Install Docker and Docker Compose in Linux Mint 21 *** --- #

--- github ---
https://github.com/ggvhcs/notes-docker
--- youtube ---
https://youtu.be/6naBDtriryE

This is the way, what I used for install docker and docker-compose on my Mint 21.
If you want to learn docker, I recommend the pelado nerd docker course in youtube.

--- Pelado Nerd Docker Course. ---
https://youtu.be/CV_Uf3Dq-EU?si=uHNlCnghLaW478jU // url pelado nerd docker course.

1- remove some package like docker or something like this.
sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get autoremove --purge docker docker-engine docker.io containerd runc

sudo apt-get remove docker.io docker-compose
sudo apt-get autoremove --purge docker docker.io docker-compose

sudo apt-get clean
sudo apt-get autoremove

2- update repository and install docker and docker-compose.
sudo apt-get update && \
sudo apt-get install -y apt-transport-https ca-certificates curl gnupg lsb-release && \
sudo apt-get remove docker docker.io && \
sudo apt install -y docker.io docker-compose

!just copy and paste the before code in the shell for install.

3- verify if docker and docker-compose are installed.
sudo apt list docker.io docker-composer
sudo aptitude search docker docker-compose

4- enable the service.
sudo systemctl start docker && \
sudo systemctl enable docker

docker --version
docker-compose --version

!I tested all this commands right now.
Uninstalling and Installing docker and docker-compose in my system. !and every thing OK.
