# FastAPI & AI Infrastructure Cost Modeler

An interactive, real-time cloud cost modeling dashboard built to estimate infrastructure expenses for high-concurrency **FastAPI** backend applications handling heavy machine learning and computer vision workloads.

![FastAPI Cost Modeler Dashboard Preview](FastAPI%20Infrastructure%20Cost%20Modeler.png)

## 🚀 Overview

When scaling modern Python applications with AI features (such as real-time object detection, YOLO pipelines, or LLM inference), traditional serverless hosting can become surprisingly expensive under heavy traffic. This tool provides instant, quantifiable insights into how traffic spikes, data payloads, and hardware selection impact your bottom line.

## 🎛️ Key Levers & Variables

* **Peak Concurrent Users:** Simulates active load driving base server scaling, database read/writes, and network traffic.
* **AI Inference Request Ratio:** Adjusts the percentage of standard CRUD requests versus heavy GPU-backed inference tasks.
* **Average Payload Size:** Models data egress and bandwidth costs (e.g., transmitting image arrays, video frames, or large JSON payloads).
* **GPU Architecture Toggle:** Evaluates cost efficiency between **Serverless / Pay-per-use** scaling and **Always-On Dedicated GPU Nodes** (e.g., AWS g4dn.xlarge instances).
* **Multi-Region High Availability:** Simulates regional failover infrastructure duplication (2x base cost multiplier).

## 💡 Key Architectural Insights

* **The Serverless Trap:** At low volumes, serverless pay-per-use compute scales efficiently to zero. However, under high sustained concurrency, dedicated GPU provisioning becomes vastly more cost-effective.
* **Bandwidth Multipliers:** High payload sizes combined with heavy data egress can rapidly become a secondary cost driver alongside compute.

## 🛠️ Tech Stack

* **Frontend UI:** HTML5, Tailwind CSS (Dark Mode Developer Theme)
* **Logic:** Pure JavaScript (Real-time dynamic calculations & relative progress bar scaling)
* **Hosting:** Static GitHub Pages / Local Deployment

## 🏃‍♂️ Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/akshayparimi18/FastAPI-Infrastructure-Cost-Modeler.git
   ```
2. Navigate to the project directory:
   ```bash
   cd FastAPI-Infrastructure-Cost-Modeler
   ```
3. Open `index.html` in any modern web browser to view and interact with the dashboard.
