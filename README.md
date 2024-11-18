# CABOT
Cartography &amp; Autonomous roBOT

## Présentation

Ce projet s'incrit dans le cadre de nos études.
Le but de ce projet est de réaliser un robot se déplacent de façon autonomme dans une pièce fermé, tout en la cartographiant, à l'aide d'un DJI RobotMaster.

![Robot Image](https://www-cdn.djiits.com/cms/uploads/db7194978c8d57a72504a3965f087fe2@374*374.png)

## Table des matières

## Installation 

### Installation ROS 

Ce projet utilise ROS2 Humble, pour l'intallation suivez ces indications :  [Lien Installation](https://docs.ros.org/en/humble/Installation.html).

### Installation Python 

La SDK du DJI RobotMaster nécessite une version python comprise entre 3.6.6 et 3.8.9
Pour ce projet nous avons décidé d'utiliser la version python 3.8.9 

La version python par defaut sur ubuntu 22 est la 3.10, il est donc necessaire d'en installer une nouvelle. 

#### Step 1 : Update server

```bash 
sudo apt update
```

#### Step 2 : Installation de python 

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```
``` bash
sudo apt install python3.8.9 -y
```

#### Step 3 :  verfication d'installation 

```bash
python3.8 --version
```
Outpout : `Python 3.8.9`

 ### Installation de la SDK RobotMaster 

Vous devez 
```bash
pip install robomaster
```
```bash 
pip install --upgrade robomaster
```


