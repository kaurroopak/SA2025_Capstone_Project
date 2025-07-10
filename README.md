# SA2025_Capstone_Project

## Dynamic Pricing for Urban Parking Lots

Capstone Project of Summer Analytics 2025 hosted by Consulting & Analytics Club × Pathway

## 🧠 Project Overview

Urban parking is a constrained resource often plagued by inefficiencies due to static pricing. To tackle this, the project implements a real-time dynamic pricing engine for 14 parking lots using data such as occupancy, queue length, traffic, and competition.

Participants build models from scratch using numpy, pandas, and Pathway to simulate intelligent, adaptive pricing systems that optimize parking space utilization.

## 🧰 Tech Stack Used

Python - Core implementation and logic

NumPy - Mathematical operations and vectorization

Pandas - Data handling and processing

Pathway - Real-time data ingestion and processing

Bokeh - Real-time visualization of pricing

Google Colab - Execution environment (notebook)

## 🗂️ Project Models

Model Description

Model 1: Baseline Linear price growth based on occupancy ratio

Model 2: Demand-Based Combines multiple features (occupancy, traffic, queue, etc.) into a demand function to set price

Model 3: Competitive (Optional) Uses geolocation and competitor pricing to fine-tune price, reroute vehicles

## 🏗️ Architecture Diagram

graph TD

A[Raw CSV Data (dataset.csv)] -->|Streamed in real-time| B[Pathway Engine]

B --> C[Feature Extraction]

C --> D[Pricing Model (Model 1 / 2 / 3)]

D --> E[Predicted Price per Lot]

E --> F[Visualization using Bokeh]

E --> G[Price History Storage]

D -->|Overload Detected| H[Vehicle Rerouting Suggestion]
🔁 Project Workflow Explanation

## Data Ingestion
-The dataset (dataset.csv) contains historical records over 73 days for 14 parking lots.

-Simulated real-time ingestion is done using a loop (or with Pathway in real use).

## Feature Extraction
-Extract relevant features: Occupancy, QueueLength, TrafficLevel, IsSpecialDay, VehicleType.

## Model Logic
Model 1: Adjust price linearly with occupancy.

Model 2: Calculate a weighted demand score, normalize it, and scale around a base price.

Model 3 (optional): Incorporate proximity and competitor pricing to strategically set prices.

## Real-Time Pricing Output
-Prices are predicted per time step for each lot.

-Bounded between $5 and $20 for realism.

## Visualization
-Bokeh plots show how price evolves per lot over the day.

-Optional comparisons across lots highlight pricing competitiveness.
