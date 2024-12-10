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

#### Pour Windows :  

Pour notre cas nous travaillons sous Ubuntu, mais il peut-être utile d'installer la bonne version de python pour réaliser des petits tests sur le robot.
Suivez les instructions sur ce [lien](https://robomaster-dev.readthedocs.io/en/latest/code_env_setup.html), dans section windows.

#### Pour ubuntu : 

##### Step 1 : Update server

```bash 
sudo apt update
```

##### Step 2 : Installation de python 


```bash
cd /usr/src
sudo wget https://www.python.org/ftp/python/3.8.9/Python-3.8.9.tgz
sudo tar xzf Python-3.8.9.tgz
cd Python-3.8.9
```
``` bash
sudo ./configure --enable-optimizations
sudo make altinstall
```

##### Step 3 :  verfication d'installation 

Verifiez que la bonne version de python à été installé.

```bash
python3.8 --version
```
Outpout : `Python 3.8.9`

 ### Installation de la SDK RobotMaster 

Vous devez l'installer après avoir installer la bonne version de python. Sinon vous aurez une erreur de ce type :
![Image-erreur](https://robomaster-dev.readthedocs.io/en/latest/_images/pip_install_error.jpg)

```bash
python3.8 -m pip install robomaster
```
```bash 
python3.8 -m pip install --upgrade robomaster
```


### Installation du project 

#### Creation d'un environnement virtuelle

Pour ce projet il est necessaire de créer un environnement virtuelle avec en version python la version python 3.8, sinon ROS utilisera la version par défault du PC. Il n'est pas forcement recommandé de changer la version par default de python, ainsi l'environnement virtuelle est la meilleur alternative 


#### blabla je sais pas le titre 

Positionnez vous dans le venv puis suivez les étapes ci-dessous. 

##### Étape 1 : Clonage du dépot git

```bash
git clone https://github.com/lorianem/Cabot.git
```

##### Étape 2 : Naviguez jusqu'au dossier 

```bash
cd Cabot
```

##### Étape 3 : Build le projet & sourcer l'environnement 

```Bash
colcon build
```
```Bash
source install/setup.bash
```

##### Étape 4 : Tester que tout fonctionne

Pour ce test allumer le robot et puis connectez vous en wifi sur celui-ci.

\\ Si vous avez un robot : 

Mettez le robot sur le bon mode comme ceci :

![image](https://github.com/user-attachments/assets/623a9d02-539a-4977-bb17-845a685d6276)

Puis connectez vous avec les identifiant normalement marqué sur le robot, ils sont de ce type : 

Identifiant : RMDEP-020202
</br> Mot de passe : 12341234

```bash
ros2 run dji test
```

Si le robot n'est pas à votre disposition : 
```bash
ros2 run test test
```


installer venv

```bash
sudo apt install python3-serial
```

```bash
python3.8 -m pip install -U pyserial
```

```bash
python3.8 -m pip install -U --user pyserial
```

```bash
mkdir -p ~/colcon_venv/src
cd ~/colcon_venv/
```

```bash
Make a virtual env and activate it 
virtualenv -p python3.8 ./venv
source ./venv/bin/activate
# Make sure that colcon doesn’t try to build the venv
touch ./venv/COLCON_IGNORE
```

```bash
python3.8 -m pip install robomaster
```

```bash
cd src
ros2 pkg create --build-type ament_python --license Apache-2.0 --node-name com dji
```

```bash
Source Humble and build
source /opt/ros/humble/setup.bash
colcon build
```

```bash
source install/setup.sh 
```

```bash
ros2 run dji com 
```


