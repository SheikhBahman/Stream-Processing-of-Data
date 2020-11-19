# Stream Processing of Data

**Stream processing:** The term "streaming" is used to describe continuous, never-ending data streams with no beginning or end, that provide a constant feed of data that can be utilized without needing to be completed or be downloaded first. Some common examples of streaming data are:

 - Real-time stock trades
 - Retail inventory management
 - Ride-sharing apps
 - Multiplayer games

![GitHub Logo](/IMG/1.png)

## Motivation

Due to the fast development of hardware and software technologies collecting data from different source can be condected more easily, precise and quick.
The world generates significant amount of data every minute of every day, and it continues to multiply at a staggering rate. Companies in every industry are quickly shifting from batch processing to real-time data stream processing to keep up with the fast evolution of data.

With the complexity of today's modern requirements, legacy data processing methods have become obsolete for most use cases, as it can only process data as groups of transactions collected over time. Modern organizations actively use real-time data streams, acting on up-to-the-millisecond data. This continuous data offers numerous advantages that are transforming the way businesses run.

## Data source
I am working on a transportation dataset from the **US Bureau of Transportation Statistics (BTS)** that is hosted as an **Amazon EBS volume snapshot**.
The dataset contains data and statistics from the US Department of Transportation on aviation, highway, transit, rail, pipeline, bike/pedestrian, and other modes of transportation in CSV format. In this Project, I concentrate exclusively on the aviation portion of the dataset, which contains domestic flight data such as departure and arrival delays, flight times, destination and origin.

- Amazon snapshot ID: snap-e1608d88
- Size: 15 GB
- 300m rows of data with 15 attributes

## System Architectures

- Download/Cleaning the data

![GitHub Logo](/IMG/2.png)

- Streaming reciveing/processing/storage

![GitHub Logo](/IMG/3.png)

- Code for ingesting the data: simulating the live data streaming

![GitHub Logo](/IMG/4.png)

- Amazon lambda function

![GitHub Logo](/IMG/5.png)

![GitHub Logo](/IMG/6.png)

## Live data processing using Spark Streaming SQL


**I have recorded the implimentation steps in the following video**

[![Watch the video](https://cdn.vox-cdn.com/thumbor/LR5ki43-jBT1N6nwkcAb4Lg0SnE=/0x0:1200x800/1220x813/filters:focal(504x304:696x496):format(webp)/cdn.vox-cdn.com/uploads/chorus_image/image/65010013/youtube.0.jpg)](https://youtu.be/-U5e7SN_v8g)

- Example of Query:
Someone wants to travel from airport X to airport Z. However, Tom also wants to stop at airport Y for some sightseeing on the way. More concretely, Tom has the following requirements:

- The second leg of the journey (flight Y-Z) must depart two days after the first leg (flight X-Y). For example, if X-Y departs on January 5, 2008, Y-Z must depart on January 7, 2008.
- Tom wants his flights scheduled to depart airport X before 12:00 PM local time and to depart airport Y after 12:00 PM local time.
- Tom wants to arrive at each destination with as little delay as possible. 

x = BOS
y = ATL
z = LAX

![GitHub Logo](/IMG/7.png)

 # Future works
 
 - Adding load balancer to receive data from different sources with different volume of ingested data 
 - Create a live dashboard such as:
       https://projects.fivethirtyeight.com/flights/
 - Adding visual root finding algorithm

