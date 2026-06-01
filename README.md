# Multi-Agent Price Intelligence System

An agentic AI system that continuously monitors product prices across multiple e-commerce platforms, predicts future discounts, and proactively notifies users when significant price drops are expected.

Designed using a multi-agent architecture with predictive analytics, business decision logic, and automated notification workflows.

## Problem Statement

E-commerce prices fluctuate frequently due to seasonal sales, promotions, inventory changes, and competitor pricing strategies.

Consumers often miss favorable buying opportunities because manually tracking prices across multiple platforms is inefficient and time-consuming.

Businesses and shoppers need an intelligent system capable of continuously monitoring prices, forecasting potential discounts, and providing proactive alerts before significant price changes occur.

## Solution Overview

The Multi-Agent Price Intelligence System combines multiple specialized AI agents with predictive machine learning models to monitor product prices, analyze historical trends, forecast future discounts, and trigger automated notifications.

The system follows a layered architecture:

- Prediction Layer
- Decision Logic Layer
- Action Layer

This architecture ensures scalable, explainable, and business-aligned decision making.

![Architecture Diagram](./assets/Multi-Agent Price Intelligence System.drawio)


## Core Components

### Frontend Dashboard

Allows users to:

- Track products
- View historical pricing
- Configure alerts
- Monitor predictions

### API Layer

Acts as the communication layer between the frontend and backend services.

### Agent Orchestrator

Coordinates interactions between specialized agents.

### Database Layer

Stores:

- Product data
- Historical prices
- User preferences
- Prediction results

## Agent Responsibilities

| Agent | Responsibility |
|---------|---------------|
| Triage Agent | Receives and validates tracking requests |
| Price Monitoring Agent | Collects prices from multiple sources |
| Product Intelligence Agent | Extracts and normalizes product information |
| Prediction Agent | Forecasts future price drops |
| Decision Agent | Applies business rules |
| Notification Agent | Sends alerts to users |

## Data Flow

1. User submits a product tracking request.
2. Triage Agent validates the request.
3. Price Monitoring Agent collects current prices.
4. Product Intelligence Agent normalizes product information.
5. Historical price data is stored in PostgreSQL.
6. Prediction Agent forecasts potential discounts.
7. Decision Agent evaluates business rules.
8. Notification Agent sends alerts.
9. User receives recommendations.

## Features

- Multi-agent architecture
- Product monitoring
- Price trend analysis
- Discount forecasting
- Rule-based decision engine
- Automated notifications
- Human review workflow
- Historical price analytics
- Scalable microservice architecture

## Human-in-the-Loop

The system includes a human review checkpoint for high-impact decisions.

Conditions requiring review:

- Prediction confidence below 70%
- Discount prediction greater than 50%
- Anomalous pricing patterns
- Insufficient historical data

Reviewers can:

- Approve alerts
- Reject alerts
- Request additional analysis

## Tech Stack

### Frontend

- Next.js
- TypeScript

### Backend

- FastAPI
- Python

### Agents

- LangGraph
- OpenAI
- LiteLLM

### Database

- PostgreSQL
- Qdrant

### Observability

- Langfuse
- OpenTelemetry

### Deployment

- Docker
- GitHub Actions
- Railway

