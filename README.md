# dynamic-pricing-urban-parking

# Dynamic Pricing for Urban Parking Lots
**Capstone Project – Summer Analytics 2025**  
Hosted by Consulting & Analytics Club × Pathway

## Overview
This project builds a real-time, intelligent dynamic pricing engine for urban parking lots using real-world demand signals such as occupancy, traffic congestion, and queue length.

It simulates a live environment using **Pathway's streaming engine**, and adjusts prices for 14 parking spaces in real time.

---

## Tech Stack
- Python (Pandas, NumPy)
- Pathway (real-time stream processing)
- Bokeh (for visualization)
- Google Colab (execution)

---

## Model Architecture

We implement 3 models:

1. **Model 1: Baseline Linear Pricing**
   - Simple linear function of occupancy

2. **Model 2: Demand-Based Pricing**
   - Considers queue, traffic, vehicle type, special days
   - Smooth, bounded pricing using normalized demand

3. **Model 3: Competitive Pricing**
   - Uses distance to nearby lots via Haversine
   - Incorporates competitor pricing logic

---

## Architecture Diagram
<pre lang="markdown"> ```mermaid graph TD A[Parking Lot Data Stream] --> B[Pathway Streaming Engine] B --> C[Feature Extractor] C --> D[Pricing Models: Model1, Model2, Model3] D --> E[Real-Time Pricing Output] E --> 
graph TD
    A[Parking Lot Data Stream] --> B[Pathway Streaming Engine]
    B --> C[Feature Extractor]
    C --> D[Pricing Models (1, 2, 3)]
    D --> E[Real-Time Pricing Output]
    E --> F[Bokeh Visualizations]
