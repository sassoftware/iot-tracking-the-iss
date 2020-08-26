# Execute the Model

This project includes two models you can execute. The `modelcsv.xml` model uses a csv file as input and executes quickly. The `model.xml` model uses a URL connector to publish the live ISS position every 10 seconds. 

## Download Files from GitLab

All files required to execute the either ISS tracking model are available in the files directory of this page. Download the following files:

- [countries2.csv](files/countries2.csv) – Polygon definitions for regions of the globe
- [iss_input.csv](files/iss_input.csv) – Input data file for modelcsv.xml
- [landmarks.csv](files/landmarks.csv) – Coordinates and radius values for landmarks around the globe
- [model.xml](files/model.xml) – Model using URL connector
- [modelcsv.xml](files/modelcsv.xml) – Model using csv file as input
- [run_iss.sh](files/run_iss.sh) – Startup script to execute model.xml (URL connector)
- [run_iss_csv.sh](files/run_iss_csv.sh) – Startup script to execute modelcsv.xml
 
## Create Server Directory

Create a server directory for the project’s files. The following is an example of the command to create a directory:

~~~bash
mkdir /home/zestem/iss
~~~

## Edit Startup Script

You must edit the startup script, `run_iss.sh` or `run_iss_csv.sh` to specify the correct server directories.

1.	Open `run_iss.sh` or `run_iss_csv.sh` with a text editor. The following is a listing of the file:

    ~~~sh
    # Register (DateFlux) ESP environment
    export DFESP_HOME=/opt/sas/viya/home/SASEventStreamProcessingEngine/6.2

    export PATH=$DFESP_HOME/bin:$PATH
    export LD_LIBRARY_PATH=$DFESP_HOME/lib:$DFESP_HOME/lib/tk:/opt/sas/viya/home/SASFoundation/sasexe:$DFESP_HOME/ssl/lib

    export PROJDIR=/home/zestem/iss

    dfesp_xml_server -http 61002 -pubsub 61003 -model file:///home/zestem/iss/model.xml -C "server.single_port_mode=true"
    ~~~
    
2.  Go to the `export PROJDIR=` line and edit the value to be the directory you created. The following is an example.    
  
    ~~~sh
    export PROJDIR=/home/zestem/iss
    ~~~

3.	Go to the last line (command to start XML Server) and edit the `-model` parameter to include the full path to the model's xml file. Ensure there are the correct number of forward slashes (/) at the beginning of the filename. The following is an example:
	
    ~~~sh
    -model file:///home/zestem/iss/model.xml
    ~~~

## Upload Files

Upload all the files to the directory you created. Change the permission of the appropriate startup script so it is executable. The following is an example of the command to do this:

~~~bash
chmod 777 /home/zestem/iss/run_iss.sh
~~~

## Execute Model

1.	Change directories to the directory containing the files you uploaded. The following is an example:

    ~~~bash
    cd /home/zestem/iss
    ~~~

2.	Type the following to execute the startup script and start the model:

    ~~~bash
    ./run_iss.sh
    ~~~

The terminal should display information about the model executing on the ESP XML Server.


