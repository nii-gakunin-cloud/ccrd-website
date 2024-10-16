---
layout: default
---


 IoT Stream Processing
<div align="center">
<a href="https://www.youtube.com/watch?v=Z0wlUi4lr6c">Introduction of Wide Area Data Collection Infrastructure (Mobile SINET) and SINETStream</a>
<br/>
<iframe width="560" height="315" src="https://www.youtube.com/embed/Z0wlUi4lr6c" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<br/>
Official Site:
SINETStream, [https://www.sinetstream.net/](https://www.sinetstream.net/)
## Overview

Big data generated by many indoor and outdoor IoT devices need to be securely analyzed in real-time for the creation of various innovative services. SINET allows construction of an end-to-end isolated HPC and IoT environment using VPN over mobile and wired networks. SINETStream is a software library which enables easy development of secure and efficient IoT applications over the environment.


## Mobile Network for IoT Applications by SINET
- The SINET Japanese R&E network has started to offer secure and high- performance VPN services over mobile and wired network (Fig.1).
- Each IoT application can construct an end-to-end isolated HPC and IoT environment using the SINET VPN.


<figure>
  <div style="text-align:center">
  <img src="figs/overview.png" alt="Mobile SINET" style="zoom:75%;" />
  <center><figcaption>Fig.1. Overview of Mobile SINET.</figcaption></center>
  </div>
</figure>

## SINETStream: Software Library for IoT Applications
- SINETStream (Fig.2) is a library for Java and Python which enables easy development of secure IoT applications.

<figure>
  <div style="text-align:center">
  <img src="figs/sinetstream_architecture.png" alt="SINETStream" style="zoom:75%;" />
  <center><figcaption>Fig.2. SINETStream overview.</figcaption></center>
  </div>
</figure>

- It provides the following capabilities:
    - User-friendly API to write and read stream data
    - Authentication and authorization
    - TLS and data encryption
    - Passive metrics collection
- Users can utilize various message brokers such as Apache Kafka and MQTT brokers.  (Fig.3)

<figure>
  <div style="text-align:center">
  <img src="figs/sinetstream.png" alt="relationship" style="zoom:40%;" />
  <center><figcaption>Fig.3. Relationship between SINETStream, message brokers and stream processing platforms.</figcaption></center>
  </div>
</figure>

## Support for Android: SINETStream Android

- SINETStream Android consists of three libraries:
    - Core library
    	- provides the SINETStream basic functions.
    	- Enables to use MQTT brokers via Eclipse Paho ([https://www.eclipse.org/paho](https://www.eclipse.org/paho)).
    - Helper library
    	- Collects data from various sensors built-in  an Android device.
    	- Publishes it via the core library.
    - Sample app
    	- Android app implemented using the helper library.
    	- allows users to collect sensors' data without development (Fig.4).

<figure>
  <div style="text-align:center">
  <img src="figs/android.png" alt="example" style="zoom:75%;" />
  <center><figcaption>Fig.4. An example application using SINETStream for Android.</figcaption></center>
  </div>
</figure>

## SINETStream Use Cases

### Secure online video processing

- We employ YOLOv3 and OpenPose for object detection and human keypoint detection, respectively.
- Image stream data captured at the sensor are sent to the cloud via the VPN, stored and analyzed in real-time.
- IoT application servers including GPU nodes are easily deployed by using [VCP](https://ccrd.nii.ac.jp/sc20/CREST/#virtual-cloud-provider-vcp).


<figure>
  <div style="text-align:center">
  <img src="figs/video-processing.png" alt="video processing" style="zoom:75%;" />
  <center><figcaption>Fig.5. Secure online video processing.</figcaption></center>
  </div>
</figure>

### Android sensors' data collection

- We develop an android app for various sensors' data collection, respectively (Fig.6).
- Data acquired by sensors equipped with SINET SIM for SINET connection can be collected and analyzed safely using a computer such as cloud connected with SINET VPN.
- Android device sensor data are accumulated in Elasticsearch via Mosquitto and Kafka, and the visualization results of different sensors can be analyzed by Kibana v7.0 for endpoint users.

<figure>
  <div style="text-align:center">
  <img src="figs/android-collection.png" alt="android app" style="zoom:100%;" />
  <center><figcaption>Fig.6. Android sensor data collection.</figcaption></center>
  </div>
</figure>

### Environment monitoring live demo

- With SINETStream you can easily develop a program that collect and analyze data from sensors distributed over a wide area network.
- The writer program running on a Raspberry Pi with temperature and humidity sensors continuously sends data to a messaging server called “SINETStream server” on AWS. 
- The reader program on AWS then receives the data from the SINETStream server and the processed data are periodically visualized [here](https://www.sinetstream.net/docs/livedemo/livedemo.en.html). 
- These programs use the SINETStream API to implement such functions as writing data from the sensor devices to the SINETStream server, and reading data from the server for visualization.

<figure>
  <div style="text-align:center">
  <img src="figs/raspi_demo.png" alt="live demo" style="zoom:85%;" />
  <center><figcaption>Fig.7. Android sensor data collection.</figcaption></center>
  </div>
</figure>

## Related Links
SINETStream Web site: [https://www.sinetstream.net/index.en.html](https://www.sinetstream.net/index.en.html)<br/>
Live demo: [https://www.sinetstream.net/docs/livedemo/livedemo.en.html](https://www.sinetstream.net/docs/livedemo/livedemo.en.html)<br/>
Tutorial: [https://www.sinetstream.net/docs/tutorial/index.en.html](https://www.sinetstream.net/docs/tutorial/index.en.html)<br/>
Promotion video: [https://www.youtube.com/watch?v=Z0wlUi4lr6c](https://www.youtube.com/watch?v=Z0wlUi4lr6c)<br/>

