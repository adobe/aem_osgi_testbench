# aem_osgi_testbench

About the Test Bench

OSGI REST Test Bench was created to provide developer examples of interacting with AEM OSGI via REST based APIs. It provides functional cases to query AEM for available workflows, running workflows, creation of workflows, resources from Sites instances as well as Assets specific content.

<img width="441" alt="image" src="https://user-images.githubusercontent.com/113538185/190446871-c89bd039-f825-404d-8e3b-b1814148990d.png">

In each API example, clicking on the ? will reveal an AJAX based example that demonstrates querying for the respective API.

<img width="344" alt="image" src="https://user-images.githubusercontent.com/113538185/190447031-d3c8e215-8bb4-4f66-bdcf-a107254fe74c.png">

Setting up the Test Bench
1.	Navigate to your WWW published directory structure.
On the Mac this may be /Library/WebServer/Documents/ (the default location)

2.	Within this location create a new directory called “osgitoolkit”

3.	Place the OSGI Toolkit HTML file into this location and rename the file “index.html”.
You should have a directory structure that looks like this:

../osgitoolkit/index.hml

4.	If not already running, start your Apache instance with this command in the shell:

sudo apachectl start

5.	Launch your browser and point it to http://localhost/osgitoolkit

You should see something that looks like below. 

<img width="327" alt="image" src="https://user-images.githubusercontent.com/113538185/190447388-f2c18c89-3cbc-4c83-93f5-47cd8611925b.png">

If not, see if any other web content is accessible or double check Apache is actually running.

With the previous steps complete, now to configure your local AEM instance to allow connections.

Configuring Adobe Experience Manager

1.	Navigate to the AEM administration panel and click on the Web Console item.
<img width="400" alt="image" src="https://user-images.githubusercontent.com/113538185/190447772-a917275e-cd5d-4dd0-baa8-a6237e3239a7.png">


2.	Search for and select the Apache Sling Referrer Filter item. Click the pencil icon to make edits that reflect below. 
<img width="402" alt="image" src="https://user-images.githubusercontent.com/113538185/190447793-4bd587cb-17c9-463a-9ca3-461863d75a98.png">

The above presumes you are running AEM on your local instance; if not make the entry reflect your instance accordingly. Make your changes and click “Save”.

3.	Next, search and select the Adobe Granite Cross Origin Resource Sharing item. Click the pencil icon to make edits that reflect below.
<img width="410" alt="image" src="https://user-images.githubusercontent.com/113538185/190447983-6f1f0348-9426-404c-9090-390d250ce057.png">

As with the previous change, note the server location may be unique to your instance. 

Additionally note the added Supported Header values.

Click Save to apply the changes.

Once changes have been applied you should be able now return to your browser. Clicking the Get Running Workflow Instances should now return a result that lists workflows that exist on your specific AEM instance.

<img width="359" alt="image" src="https://user-images.githubusercontent.com/113538185/190448107-052f2f28-66d9-4cb9-b194-2184fc3a12b3.png">

You should see a response output to the results field as shown below:

<img width="504" alt="image" src="https://user-images.githubusercontent.com/113538185/190448174-60d0e61f-f160-40bc-a0b7-3f385c4e4f9c.png">

Optional

While not required, if you want to run the Trigger Full Workflow instance, the sample payload included contains elements aligned with the “Simple Assign Workflow”. Using the package manager, install the package to add that workflow model to your instance.

<img width="360" alt="image" src="https://user-images.githubusercontent.com/113538185/190448257-341ba5a7-858f-4992-a1ca-1e96ee4c7b0e.png">







