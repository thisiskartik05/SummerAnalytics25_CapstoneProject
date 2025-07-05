# SummerAnalytics25_CapstoneProject

[Open in Google Colab](https://colab.research.google.com/drive/1g2rIrmHVy-cyw6pD2q-fIciXte6aLc95?usp=sharing)


# Dynamic Parking Pricing System

A real-time simulation of smart parking pricing across multiple lots using streaming data and adaptive pricing models.

This project compares three models:

- Model 1: Linear Pricing based on Occupancy
- Model 2: Multi-Factor Demand-Based Pricing
- Model 3: Competitor-Aware Pricing using Geographic Proximity

The system is built for a capstone submission under Summer Analytics, integrating real-time data processing with rich visual analytics.

---

## Tech Stack

| Layer            | Tools / Frameworks                                  |
|------------------|-----------------------------------------------------|
| Data Streaming   | Pathway (real-time stream processor)                |
| Data Analysis    | Python, Pandas, NumPy                               |
| Visualization    | Bokeh, Matplotlib                                   |
| Geo Computation  | Haversine Formula (for geo-aware pricing)           |
| Packaging        | LaTeX (for report), JSON (for nearby map cache)     |

---

## Architecture Diagram (Mermaid)

```mermaid
graph TD
    A[CSV Input] --> B(Pathway Streaming Engine)
    B --> C{Pricing Logic}
    C -->|Model 1| D1[Occupancy-Based Linear Price]
    C -->|Model 2| D2[Multi-Factor Demand Score]
    C -->|Model 3| D3[Competitor-Aware Geo Price]
    D1 --> E[model1_price.csv]
    D2 --> E2[model2_price.csv]
    D3 --> E3[model3_price.csv]
    E3 --> F[Bokeh Dashboard]
    subgraph Visualization
        F --> G[Interactive Plots]
    end
