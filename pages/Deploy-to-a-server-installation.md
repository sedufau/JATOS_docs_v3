---
title: Deply to a server installation
keywords: create, import, export
tags:
summary:
sidebar: mydoc_sidebar
permalink: Deploy-to-a-server-installation.html
folder:
toc: true
last_updated: 20 Nov 2019
---


### Import / Export of studies
Usually you conveniently develop your study on your local computer where you have a [local installation of JATOS](Installation.html). Then just use the export and import buttons in your installations to transfer the study to your [JATOS server](JATOS-on-a-server.html).


If you have a server already, you will need to take your ready-to-run study from your local installation and deploy it to the server. In order to do this:
1. On your *local* JATOS installation, where your study is, click on the study you want to export on the left sidebar. 
1. On the Study bar, click Export. A pop-up window will appear. Save the .jzip file wherever you like on your computer.  
1. On your *server* installation, simply click Import. 

Here's a little sketch of the same three steps above
![jzip workflow](images/jzipWorkflow.png)

Please note that:

* The two JATOS look almost identical, and you will (basically) only distinguish them on the basis of the URL in the browser. To prevent confusion, we've made it easier: A local JATOS installation has a black bar on top. A server installation has a light-grey bar. 
* A .jzip file is a normal .zip file. We just changed the name to make this process clearer. (JATOS users got confused and often tried to unzip the file they had downloaded, add HTML files in it, and re-zip it. This will lead to all sorts of problems. Don't do this. 
You should do all modifications of files and study properties from the JATOS GUI.)
* In the process of exporting/importing you'll be moving all HTML/JS/CSS files, along with any assets (images, audio, etc) contained in the local study folder. You will also move the study and component properties (whether it's a group study, allowed worker types, HTML files associated with each component, and much more). You will **not** move result data. 
* If you want to make changes to a study, we also recommend that you do that locally, then again Export locally->Import into the server. If you do this, there will be one more step where you have to confirm that and whether you want to replace the study assets properties.

If you have trouble with the export and you are using a Safari browser have a look into [this issue in our Troubleshooting section](Troubleshooting.html#downloading-a-study--exporting-a-study-fails-eg-in-safari-browsers).




### Decide how you're going to recruit your workers and generate the links
Once you have your study running and have it on a server instance, you'll need to get your workers to access your study. [Different types of workers](Worker-Types.html) might be allowed to run your study. You could, but you don't have to, recruit your workers [using MTurk](Connect-to-Mechanical-Turk.html). You could also generate direct links in the [Worker Setup](Run-your-Study-with-Batch-Manager-and-Worker-Setup.html) to send to different workers. 

### Export your result data
After you let workers run your study and you gathered result data you probably want to export them to your local computer for further analysis. Go to one of the **Results** views and select the results you want to export (select them by just clicking somewhere in the row). Then click 'Export Selected'. This will download all your results in one text file. 

### Analyse your data
Once you have collected all your data, export it to text files. If you used the JSON format (which is handy - but any other text is fine too) you can analyse your data using this nice [JSON parser for Matlab and Octave](http://iso2mesh.sourceforge.net/cgi-bin/index.cgi?jsonlab) or the [JSON parser for R](http://cran.r-project.org/web/packages/jsonlite/index.html).