# hadoop-box


## Download the Vgrant Box File from the following link:

      https://drive.google.com/drive/folders/1lLMVmuFIUq-CyNfXmTs56crxXodMn3Bs?usp=sharing
      
      Here you will see two files:
      
      1. package.box
      2. vagrant.zip

## Extract both files in a single folder  in below location

      work/boxes/hadoop-vm/
      
## Then you will see the below structure like single folder

      ./Vagrantfile
      ./Data/
      ./docs
      ./package.box
      
      
## Then Issue the below commands

      vagrant box add package.box --name hadoop-machine
## Then issue the below commands

      Optiona: If you are installed the bgguest plugin
      
      vagrant plugin install vagrant-vbguest
      
      OR You can install directly the below commands
   
      vagrant plugin update vagrant-vbguest
      
      
## Then issue the below command to up the machine

      vagrant up
      
##. Then if the above command successful, you can up the get into the machine using the below command

      vagrant ssh
      
##. How to start the service

### Issue the below command for starting Mysql, Hadoop and Presto Services

      ./servers_start.sh 
      
## Then start the hive meta-store using the below command in seperate vagrant terminal:

       hive --service metastore
       
## Then start hive server using the below command in seperate vagrant terminal:

      hiveserver2
      
## Then start the hive beeline cli for interactive the hive catalogs and tables:

      beeline -n vagrant -u jdbc:hive2://localhost:10000
      
## Then start the presto cli to interactive with Hive Catalogs:

      presto/presto-server-332/bin/presto --server localhost:8080 --catalog hive --schema tutorials
      
## Then start the presto cli to interactive with mysql Catalogs:

      presto/presto-server-332/bin/presto --server localhost:8080 --catalog mysql --schema default
      
Please call your admin/lead if you have any troubles or questions.

Happy Coding :)
      
