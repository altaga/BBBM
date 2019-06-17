# BBBM : Brainium Bridge Baby Monitor for predictive maintenance

The little monitoring that bridges have in most countries in the world, and the structural damage that they can have over time and as the lack of preventive maintenance can cause a partial or total failure of the bridge. 

The main problems by which a bridge can fail and fall are: 

 - Infrastructure failure.
 - Structural collapse.
 - Lack of good maintenance.
 - Wear and Tear - Floods. 
 - Unexpected events.
 - A combination of issues. 

According to the 2017 Infrastructure Report Card published by the American Society of Civil Engineers (ASCE), almost 40 percent of the 614, 387 bridges in the United States are at least a half century old. Almost 10 percent were structurally deficient in 2016. On average, 188 million vehicles cross structurally deficient bridges each day. People who manage them are constantly looking for more cost-effective ways to keep them in good repair.

Perhaps the biggest issue affecting people who maintain bridges today is that they are forced into being reactive in how they approach their work, rather than proactive. They must repair the worst damage to structures rather than use limited resources to keep them in good shape. As with most things, being reactive is never as effective as planning ahead.

A “worst first” approach is not a cost-effective way to keep bridges healthy. It evolves into a vicious cycle where more and more budget dollars go toward emergency repairs. This under-funds proactive maintenance projects that could keep bridges out of the deficient category entirely.

According to ASCE, the current cost to rehabilitate the nation’s bridges is more than $120 billion. As with most things earthquakes and other disasters also can suddenly pass and if there's not a precise monitoring, issues could be fatal.

And well, this is a very personal problem. On September the 7th of 2017 there was an earthquake in Mexico City. At about 8.1 in the Richter scale it caused structural damage to several buildings around the city and a couple pedestrian bridges in the my University. This was the result:
[![SGD](https://allthatsinteresting.com/wordpress/wp-content/uploads/2018/03/tacoma-narrows-man-og.jpg)](https://www.youtube.com/watch?v=eVkoiONCB8s)

Sorry github does not allow embed videos.

With better monitoring and alert systems we could have probably spotted on these failures and prevented the crisis, or maybe acted on it faster.

# Table of contents

* [Introduction](#introduction)
* [Materials](#materials)
* [Connection](#connection)
* [Train](#train)
* [IFTTT](#ifttt)
* [Demo](#demo)
* [Comments](#comments)
* [References](#references)

## Introduction:

Our solution will be to place vibration sensors (using the SmartEdge Agile’s accelerometer and gyroscope) strategically in bridges to perform continuous monitoring. And through AI and Machine Learning at the edge we will generate predictive models for the wear and tear of the bridge, and will provide the user recommendations and notifications in addition to a dashboard to schedule preventive maintenance. 

Current bridge monitoring systems are exclusively for sensor monitoring and information deployment to the user, most of the time they have to go to the bridge directly and check on the displays the information that the sensors provide. In the case of bridges the engineer in charge and if these systems have some processing in the Cloud, it is only for the aesthetic deployment of the information of the sensors, but this is very rare and not a common occurrence.

Some examples are these companies: - https://www.campbellsci.com/structural-health-monitoring - http://alliancesensors.com/bridge-monitoring-systems This solution will result in: - Less spending on excessive maintenance of the bridges. - Point out critical areas where the bridge is experiencing more wear. - Avoid structural damage that may be critical or fatal to bridges. - Generate more trust between customers and users of bridges.

<img src="https://pbs.twimg.com/media/DrCtqQrVAAAT7Ky.jpg:large" width="400">

## Materials:

List the hardware and software you will use to build this.

Hardware: 
- SmartEdge Agile
- Laptop or Desktop PC. 

Software: 
- Brainium Portal. (https://spa.brainium.com/signup/login)
- Smartphone APP Gateway. (https://play.google.com/store/apps/details?id=com.brainium.android.gateway&hl=es_MX)
- IFTTT. (https://ifttt.com/discover)

Optional Hardware:

- Arduino UNO.
- Servomotor.
- Buttons.

Optional Software:

- ArduinoIDE.

## Connection:

The first step to realize this project is to create a brainium account and add your first device, all the images and instructions to configure our device were obtained from the official guide of Brainium. (https://brainium.blob.core.windows.net/public/docs/User%20manual%20Brainium%20Portal.pdf)

1. Install and connect your environment:

1.1.Create a web account:

 - Go to https://www.brainium.com/portal and select ‘sign up’.
 - You will receive a key by e-mail, use it to validate your account creation.
 
 <img src="https://i.ibb.co/gTVr5G2/sing.png" width="1000">
 
1.2.Install your gateway:

https://play.google.com/store/apps/details?id=com.brainium.android.gateway&hl=es_MX

You can use an iOS, Android (phone or tablet), or a Linux Raspberry PI to act as a Gateway
for your Brainium solution and connect your SmartEdge Agile device to Brainium Cloud.

For iOS and Android gateway you need to install Brainium Gateway mobile app. There are
two ways to get Brainium gateway mobile application:

1) Scan QR code located on the Agile device packaging. You will be redirected to the
needed mobile app download page. If redirect brings you to www.brainium.com/apps,
tap on “Get it” button for iOS or Android.

2) Open the Equipment page on Brainium and click on “Get it” button for iOS or Android
to be redirected to the mobile app download page.

For Linux gateway, open the Equipment page on Brainium and click the “Get it” button for
Linux gateway. You will be redirected to www.brainium.com/apps/linux containing all the
instructions to download and install the Linux gateway application.

Install Brainium iOS, Android, or Linux gateway; then enter the gateway application with the
same credentials you used when registering on the web portal. Then your gateway will
appear in the web app list of gateways (Equipment → Gateways).

1.3.Pair Agile device:

Turn on your Agile device by pressing the button for more than 2 seconds. When device is
turned on, it will start blinking with blue light.

Note: If you turn on the device while being in charge, you will see one LED in red for charge
indication and one LED blinking blue at the same time. For detailed description of Agile
device light indication and button behavior see Know your Agile device section below.

Ensure that Brainium Gateway is always visible on your mobile, no screen lock (for iOS app
as it will not work in background). Ensure the Brainium Gateway is connected to the cloud.

Go to Brainium portal ‘Equipment’ page. You will see your gateway ID and gateway name.
The name can be changed as needed while ID always remains the same.

Press ‘+’ to connect the Agile device.

 <img src="https://i.ibb.co/j56Zdy2/bbbbm.png" width="1000">

You will be asked to accept the terms of Brainium discovery period. After that, each device
you add to the portal for the first time will have the following limits:

- up to 180 days of usage,
- up to 15GB of re-usable cloud storage,
- up to 2GB of telemetry tracking traffic.

Select your device in a list and click on “Connect” (Connection will be established in 20-30
seconds).

<img src="https://i.ibb.co/Ybcx6Nh/device1.png" width="1000">

Now you can rename your Agile device, view it in the list of devices and add it to your
project.

1.4.Firmware update:

Brainium Portal allows user to keep his device updated and push a new firmware for all the
users by using “Firmware Over the Air” update functionality.

You can get 2 types of updates: mandatory (the user will see a notification right after the
pairing and update will start automatically without user approval) and non-mandatory (the
user has possibility to choose whether/when she/he wants to update the device or not).

Go to Equipment → Device to check if any new FW is available. You can see a notification
on the page header also. 

The update will start when click the icon . The icon will change its state showing an update
progress:

After the firmware downloading, the icon will change its state again notifying the user about
device rebooting:

Important note: when firmware rebooting process is started don’t turn off the device and
gateway till the completion of the firmware update.

When updating process is finished you will get a notification message. Update icon will
disappear until a new firmware version is available. 

## Train:

  - We created a new workspace.
  
<img src="https://i.ibb.co/9rGSVnX/WS1.png" width="1000">

  - We give the project a name.
  
  <img src="https://i.ibb.co/cCvszMs/WS2.png" width="1000">

  - We select the device that will obtain the patterns of the machine.
  
  <img src="https://i.ibb.co/nfK3wCQ/WS3.png" width="1000">

  - In our case we connect the machine to our bridge simulator, as you can see in the following video to detect oscilation patterns.

[![SGD](https://img.interempresas.net/fotos/1843350.jpeg)](https://youtu.be/cFr_DeH4-iQ)

Sorry github does not allow embed videos.

- Once we have a large sample of patterns, we rename the patterns that are relevant to our model and we create the model.

<img src="https://i.ibb.co/qr4hqsf/Capture11.png" width="1000">

The patterns we recorded were the following, the most important for us and our notification that predictive maintenance is required is Max Vibration S:

- S1: Static State.
- Med Vibration S.
- S2: Static State.
- Max Vibration S.
- S3: Static State.

- Once the model is created, we go to the projects tab and create a new one.

<img src="https://i.ibb.co/Wyz3VrH/tab.png" width="1000">

- We assign to our project the BBBM device.

<img src="https://i.ibb.co/1Xb4kCB/bbbbbbbm.png" width="1000">

# IFTTT:

- First we need to create an account in IFTTT, fortunately Brainium has an integration with this platform for integration of services.

<img src="https://i.ibb.co/Bf9cYLg/Capture1.png" width="1000">

- We search for "Brainium" in the search bar.

<img src="https://i.ibb.co/tDLgCLW/Capture2.png" width="1000">

- We enter any of the applets and press on the author Brainium.

<img src="https://i.ibb.co/KbR8SJ8/Capture3.png" width="1000">

- We select "Connect" to make the connection with the Brainium platform.

<img src="https://i.ibb.co/SxMmKXB/Capture45.png" width="1000">

- We put our credentials to connect.

<img src = "https://i.ibb.co/LJ5R4MH/Capture55.png" width = "1000">

- We allow the access.

<img src = "https://i.ibb.co/6rg7qqx/Capture56.png" width = "1000">

- We selected the Applet "Get all Brainium alerts on your device".

<img src = "https://i.ibb.co/y42CbmL/Capture57.png" width = "1000">

- Turn ON and thats all!

<img src = "https://i.ibb.co/sJ23cFV/Capture58.png" width = "1000">

- To finish this, we need to install the IFTTT app on your device.

https://play.google.com/store/apps/details?id=com.ifttt.ifttt&hl=es_MX

## Demo:

En este video presentaremos el demo de nuestro producto y ademas mostraremos como fue nuestra busqeda por la mejor AI para realizarlo, porfavor disfrutenlo.



Video: Click on the image:

[![SGD](https://media.giphy.com/media/9VeuJ8sII8rYD7XViE/giphy.gif)](https://www.youtube.com/watch?v=uu8WHsOgXgg)

Sorry github does not allow embed videos.

* [Table of Contents](#table-of-contents)
