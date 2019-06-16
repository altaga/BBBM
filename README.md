# BBBM

What problem are you going to solve?
The little monitoring that bridges have in most countries in the world, and the structural damage that they can have over time and as the lack of preventive maintenance can cause a partial or total failure of the bridge. The main problems by which a bridge can fail and fall are: - Infrastructure failure.
 - Structural collapse - Lack of good maintenance - Wear and Tear - Floods. - Unexpected events - A combination of issues. 

According to the 2017 Infrastructure Report Card published by the American Society of Civil Engineers (ASCE), almost 40 percent of the 614, 387 bridges in the United States are at least a half century old. Almost 10 percent were structurally deficient in 2016. On average, 188 million vehicles cross structurally deficient bridges each day. People who manage them are constantly looking for more cost-effective ways to keep them in good repair.

Perhaps the biggest issue affecting people who maintain bridges today is that they are forced into being reactive in how they approach their work, rather than proactive. They must repair the worst damage to structures rather than use limited resources to keep them in good shape. As with most things, being reactive is never as effective as planning ahead.

A “worst first” approach is not a cost-effective way to keep bridges healthy. It evolves into a vicious cycle where more and more budget dollars go toward emergency repairs. This under-funds proactive maintenance projects that could keep bridges out of the deficient category entirely.

According to ASCE, the current cost to rehabilitate the nation’s bridges is more than $120 billion. As with most things earthquakes and other disasters also can suddenly pass and if there's not a precise monitoring, issues could be fatal.

And well, this is a very personal problem. On September the 7th of 2017 there was an earthquake in Mexico City. At about 8.1 in the Richter scale it caused structural damage to several buildings around the city and a couple pedestrian bridges in the my University. This was the result:
https://www.youtube.com/watch?v=eVkoiONCB8s

With better monitoring and alert systems we could have probably spotted on these failures and prevented the crisis, or maybe acted on it faster.

What are you going to build to solve this problem? How is it different from existing solutions? Why is it useful?
Our solution will be to place vibration sensors (using the SmartEdge Agile’s accelerometer and gyroscope) strategically in bridges to perform continuous monitoring. And through AI and Machine Learning at the edge we will generate predictive models for the wear and tear of the bridge, and will provide the user recommendations and notifications in addition to a dashboard to schedule preventive maintenance. 

Current bridge monitoring systems are exclusively for sensor monitoring and information deployment to the user, most of the time they have to go to the bridge directly and check on the displays the information that the sensors provide. In the case of bridges the engineer in charge and if these systems have some processing in the Cloud, it is only for the aesthetic deployment of the information of the sensors, but this is very rare and not a common occurrence.

Some examples are these companies: - https://www.campbellsci.com/structural-health-monitoring - http://alliancesensors.com/bridge-monitoring-systems This solution will result in: - Less spending on excessive maintenance of the bridges. - Point out critical areas where the bridge is experiencing more wear. - Avoid structural damage that may be critical or fatal to bridges. - Generate more trust between customers and users of bridges.

How does your solution work? What are the main features? Please specify how you will use the SmartEdge Agile in your solution.
This aim project is to make a safety monitoring system by  analyzing natural vibration patterns on bridges.

 Features: - Edge Computing. - Plug and Play. - Modular Sensors. - Data Analytics Dashboards (WebApp). 

Through these components, we will determine the natural frequency of the bridge with the real-time data of the sensors, making an extrapolation as accurate as possible through the machine learning model provided by Brainium’s AI suit, once with this data, we can determine at what points of the day the bridge suffers more wear due to vibration frequencies which approximate the natural frequency and through ML algorithms make an approximation of the wear of these bridges over time and when the preventive maintenance should be carried out to avoid structural failures due to the compression efforts caused by this phenomenon. Basically the triple suit of services provided by the SmartEdge Agile would be used to run said ML algorithms to provide insights to this case.

Using Azure and some other tools we would create a dashboard to monitor everything.

List the hardware and software you will use to build this.
Hardware: 

-SmartEdge Agile
- Accelerometers (provided by the SmartEdge Agile). 
- Vibration Sensors (gyroscope).
- Laptop or Desktop PC (To make an Apache server to perform the data deployment through html5.) 
- Portable battery or power source for the System (I know the SmartEdge Agile has a battery but it is quite small at 250mAh). 

Software: 
-Brainium Portal
-Fusion 360 (to Design 3D weatherproof Cases).
-XAMPP control panel
- Microsoft Azure IoT hub
