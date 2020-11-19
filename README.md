# Stream Processing of Data

**Stream processing:** The term "streaming" is used to describe continuous, never-ending data streams with no beginning or end, that provide a constant feed of data that can be utilized without needing to be completed or be downloaded first. Some common examples of streaming data are:

 - Real-time stock trades
 - Retail inventory management
 - Ride-sharing apps
 - Rultiplayer games

![GitHub Logo](/IMG/1.png)

## Motivation

Due to the fast development of hardware and software technologies collecting data from different source can be condected more easily, precise and quick.
The world generates significant amount of data every minute of every day, and it continues to multiply at a staggering rate. Companies in every industry are quickly shifting from batch processing to real-time data stream processing to keep up with the fast evolution of data.

With the complexity of today's modern requirements, legacy data processing methods have become obsolete for most use cases, as it can only process data as groups of transactions collected over time. Modern organizations actively use real-time data streams, acting on up-to-the-millisecond data. This continuous data offers numerous advantages that are transforming the way businesses run.

## Data source
I will work on a transportation dataset from the **US Bureau of Transportation Statistics (BTS)** that is hosted as an **Amazon EBS volume snapshot**.
The dataset used in the Project contains data and statistics from the US Department of Transportation on aviation, highway, transit, rail, pipeline, bike/pedestrian, and other modes of transportation in CSV format. In this Project, I will concentrate exclusively on the aviation portion of the dataset, which contains domestic flight data such as departure and arrival delays, flight times.

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




 
