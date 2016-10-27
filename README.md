# Vagrant Flask Template

![N|Solid](http://i.imgur.com/2raGNAE.gif)

#### Vagrant Flask Template integrates, with as little as possible code/configuration, the following:
  - Python, 
  - Flask
  - Vagrant(virtualbox) 

#### Requirements
The following applications are required to run the Vagrant Flask Template
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

If developing on Windows you will need to use an additional application in order to SSH into the box (explained later)   
I'd recommend using the Git Shell packaged with the [Github Desktop](https://desktop.github.com/) Application

#### Setup Instructions
1) Clone this repository. More info at [How to Clone a repository](https://help.github.com/articles/cloning-a-repository/)

2) Follow these commands on terminal or git bash/git shell
```sh
# cd into the repository root (top level of the repository where Vagrantfile is)
$ Vagrant up
$ Vagrant ssh
# Now you have established an SSH connection with the dev box
$ python ./app/flaskhelloworld.py
```
3) Navigate to the following address on your browser of choice: [localhost:5000](localhost:5000)
