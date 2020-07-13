# Repo Fully Automated

### Jenkins Interface

- A pipeline has been created through Jenkins and associated web hooks to this repo
- Once any changes to the code are made, it is committed and pushed to the development branch
- Jenkins reads the code and this triggers a new build
- Once the vm is successfully built, a trigger is set on Jenkins for the changes to the development branch to be merged with the master branch
- The integrated machine can now be tested for use

# Using your virtual machine

### Creating the vm

- in bash/gitbash type the following cmd:

````
   vagrant up

 ````

 - Wait for the machine to be created. If there are any errors, vagrantfile or provisioning scripts need debugging

 - start and access the virtual machine with the following command:

 ````
 	vagrant ssh app

 ````

 - Once inside the machine, enter the following command:

 ````

 	cd ..

 ````

 - this will take you to the home directory where you need to access the app directory:

 ````
 	cd ubuntu/app

 ````

 - check that npm  is installed with the following command:

 ````
 	npm --version

 ````

 - the version number should load on a separate line (e.g. 3.10.10)

- start npm by using the following command:

````
	npm start

````

- Once you get a message "listening on port 3000", you can now test the functionality on a web browser by entering the following in the URL bar:

````
	development.local:3000

````

- you can now test if the database has been seeded:

````
	development.local:3000/posts

````

Errors should be logged and escalated for immediate resolution 

````
	cd ..
	cd home/ubuntu/app/seeds

	node seed.js

	cd ..

	npm start

````
- The above script is just in case the database was not seeded manually

