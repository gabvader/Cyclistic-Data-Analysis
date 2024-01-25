### **Welcome to Cyclistic Data Analysis!** 
This Notebook describes the steps I have taken along my way to complete the Google Analytics Capstone Project. It has been a tough but nevertheless rewarding process, with plenty of challenges and opportunities to apply, consolidate and delve into the new skills of data analysis I have been introduced into during the course. I hope you have fun while checking on this Notebook, and now, let's dive straight into the Cyclistic Data Anaysis!

## Background
**Cyclistic** is a **bike-share program** that features more than 5,800 bicycles and 600 docking stations in **Chicago**. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day.

Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as **casual riders**. Customers who purchase annual memberships are **Cyclistic members**.

Cyclistic's finance analyst concluded that **members are much more profitable than casual riders**. Maximizing the number of annual members will be key to future growth, and there might be a very good chance to **convert casual riders into members**. 

We will use the Cyclistic’s historical trip data spanning from 2019.01 to 2023.11, as available in (https://divvy-tripdata.s3.amazonaws.com/index.html).
For geographical analysis, we will use  the data for the localization of **Chicago neighborhoods**, as downloaded from the [Chicago Data Portal](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Neighborhoods/bbvz-uum9).

In order to design marketing strategies aimed at converting casual riders into annual members, we nned to better **understand how members and casual riders** differ. That is the aim ouf our study, to answer the question: 
**How do annual members and casual riders use Cyclistic bikes differently?**
Let's go for it and start our analysis!

## Table of Contents 📖
* [Set up Notebook 📘](#chapter1)
* [Import Data 🗃️](#chapter2)
* [Exploring and Understanding Data 🔎](#chapter3)
* [Get the Data Together! – Wrangling and Combining Datasets 🔄](#chapter4)
    * [Custom function for reading monthly tables in yearly list](#subsection4_1)
    * [Creating a dataset for years 2021 – 2023](#subsection4_2)
* [Cleaning and Sorting Data 🧹](#chapter5)
    * [Dropping NA values?](#subsection5_1)
    * [Checking Usertype Data](#subsection5_2)
    * [Setting and Sorting Time](#subsection5_3)
    * [Checking for Duplicates in `ride_id`](#subsection5_4)
* [Analyzing our Data 📊📉📈](#chapter6)
    * [1. Member / Casual Riders Usage](#subsection6_1)
    * [2. Comparative Analysis on Ride Duration](#subsection6_2)
    * [3. Comparative Analysis by Yearly Months](#subsection6_3)
    * [4. Comparative Analysis by Weekday](#subsection6_4)
    * [5. Comparative Analysis by Daily Hours](#subsection6_5)
    * [6. Comparative Analysis by Rideable Type](#subsection6_6)
    * [7. Most Used Stations](#subsection6_7)
