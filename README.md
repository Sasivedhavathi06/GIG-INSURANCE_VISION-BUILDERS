# GIG-INSURANCE_VISION-BUILDERS
AI-powered parametric insurance platform that protects gig delivery workers from income loss caused by external disruptions such as extreme weather and environmental conditions.
# Overview
Delivery workers face many risks during their daily work such as accidents, extreme weather conditions, vehicle breakdowns, and income instability. Traditional insurance processes are slow and require manual claim verification.
Our project proposes an AI-powered parametric insurance platform that automatically provides financial support to delivery workers when predefined conditions occur. Instead of filing manual claims, payouts are triggered automatically based on real-time data such as weather conditions, delivery activity, and accident reports.
The goal of this system is to provide fast, transparent, and automated insurance protection for delivery workers.
# Problem Statement
Gig delivery workers depend on daily work availability. When disruptions occur:
Heavy rainfall stops deliveries

Severe pollution prevents outdoor work

Flooded roads block delivery routes

Extreme temperatures reduce working hours

These disruptions can reduce 20–30% of a worker's weekly income, and currently workers bear the full financial loss.

Traditional insurance systems are not suitable because they require manual claims and slow processing
# Proposed Solution
The proposed solution is to develop an AI-powered parametric insurance system for delivery workers that provides instant compensation when disruptions affect their ability to earn.

How the Solution Works

The system continuously monitors external conditions such as:

Weather conditions (rain, storm)

Traffic congestion

Unexpected incidents (accidents, roadblocks)

When any of these conditions cross a predefined threshold:

The system automatically:
Detects the disruption

Estimates the income loss

Triggers compensation instantly
 # Key Idea (Parametric Insurance)
 The platform evaluates risk using:

Location data

Weather conditions

Historical earnings

Work activity
# Weekly Premium Model
The platform follows a weekly premium model so that delivery workers can afford insurance easily.

Plan	Weekly Premium	Coverage

Basic Plan	₹20	Rain delay support

Standard Plan	₹40	Accident and delay support

Premium Plan	₹70	Full coverage

Premiums may change based on AI-based risk assessment.

Benefits of the weekly model:

•	Affordable for gig workers

•	Flexible payment structure

•	Easy enrollment
# Parametric Triggers
Parametric insurance gives automatic compensation based on certain conditions, without any manual claim process.
Triggers

Heavy Rain → Rainfall above limit → ₹300

Accident → Accident detected/reported → ₹2000

Severe Traffic → Delivery delay due to traffic → ₹200

Benefit

Instant payout

No paperwork

Simple and fast process
# Persona Based Scenario
Name: Rahul

Age: 26

Occupation: Food Delivery Partner

Scenario

Rahul works as a delivery partner and depends on daily deliveries for income.

Rahul downloads the insurance platform and registers.

He selects a weekly premium plan.
	
The system monitors real-time data like weather and delivery activity.
   
One day heavy rainfall affects deliveries.
	
The system automatically detects the weather condition.
	
A parametric trigger activates, and Rahul receives compensation automatically without submitting any claim.

This ensures Rahul has financial support during difficult conditions
 # System Architecture

The platform uses an event-driven architecture built around Kafka and Redis.

Worker actions and environmental events are published to a Kafka event streaming system, enabling services to process events asynchronously.

Core services include:

Risk Engine (AI-based premium calculation)

Trigger Engine (detect disruption events)

Fraud Detection Service

Claim Processing Service

Payout Service

Redis is used as a real-time caching layer for policy data, worker activity, and disruption monitoring.
# Architecture Diagram

<img width="1411" height="788" alt="image" src="https://github.com/user-attachments/assets/baa39633-e6a1-4141-aacd-6f7f07ad4bec" />

# Core Components

Worker App

Allows gig workers to register, purchase policies, and track coverage.

Backend API

Handles user requests and publishes events to Kafka.

Kafka Event System

Central message broker enabling event-driven communication between services.

Risk Engine

Uses AI models to calculate disruption risk and determine weekly premium pricing.

Trigger Engine

Detects environmental disruption events and initiates automatic claims.

Fraud Detection

Validates worker location, activity patterns, and claim legitimacy.

Claim Service

Handles automated claim processing.

Payout Service

Simulates payout through a payment gateway.

Redis Cache

Stores real-time policy data and disruption monitoring information


