---
layout: post
title:  "My internship in a medical Research Centre"
date:   2022-09-19 16:45:00
blurb: "A look at an example post using Bay Jekyll theme."
og_image: /assets/img/content/post-example/cermel.png
---

<img src="{{ "/assets/img/content/post-example/cermel.png" | absolute_url }}" alt="bay" class="post-pic"/>
<br />
<br />

Here is a brief presentation of my mission as an intern at CERMEL Research Centre in Gabon.

Importing data from biomedical analysers to the Laboratory information system is something as crucial as complicated for the Centre, since those biomedical analysers communicate with their host per serial connection and not per Ethernet cable. Therefore, to avoid over-relying on the printer and losing dozens of results, the point will be to deal with such a type of connection to lead the data to the database of the software used by the laboratory[^1].

<br />


#### Table of Contents
1. [Serial Connection](#part-1)
    * [From analysers to serial data converter](#part-2-sub-part-1)
    * [From serial data converter to the software](#part-2-sub-part-2)
2. [Modules Implementation](#part-2)
3. [Footnotes](#footnotes)

#### Serial Connection
To achieve serial connection to the server of the software, one important thing was to develop a synchronisation per RS232 serial cable with respect to several parameters between the biomedical analysers and a PC. Once this step got mastered, the second one has been to use a certain device as transition for data to let them reach the server.

<br />

##### From analysers to serial data converter
Firstly, the challenge was to synchronise serial parameters on the analysers and on the serial data converter, so that by connecting them per cable, they could exchange information. Once the serial data converter has been able to receive data from the analysers, it could have been possible to use it as a bridge by which the information could go through in order to reach the server.

<br />

##### From serial data converter to the software
Then, another task to handle was to make the connect to the server as a client by giving it the address and the port of the server. Right after that, using the Ubuntu distribution of the server to check the log activity allowed to have a look on how the system received the information coming from the converter, hence, from the analysers, which solved the automated data transfer issue.

<br />
<br />

#### Modules Implementation
Finally, one last thing was to implement for the software new Python modules in object-oriented programming to make it recognize the messages from the new analysers and parse the elements of those that would be kept for the database.  
<br />


##### FOOTNOTES

[^1]: SENAITE is the name of the Software and the product of the company Riding Bytes.
