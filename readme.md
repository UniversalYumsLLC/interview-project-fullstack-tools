# Subscription Box Inventory Analysis Project

## Background

We are a subscription-based snack box company that sends monthly boxes with snacks from different countries. In this project scenario, the company is experiencing growth and needs to ensure inventory levels are sufficient to meet demand for upcoming months.

The company has three subscription tiers:

- **SUBSMALL** - Small box
- **SUBMEDIUM** - Medium box
- **SUBLARGE** - Large box

Each month features a default box from a specific country:

- June 2025: Taiwan (TWN25)
- July 2025: Czech Republic (CZE25)
- August 2025: Indonesia (IDN25)
- September 2025: Mexico (MEX25)

Customers can either receive the default box for the month or select custom boxes from other series (KORAA, ITAA, GRCAA) when they start their subscription.

## Project Objective

Your task is to build a tool that analyzes subscription and inventory data to identify potential shortages for the upcoming months. The tool should:

1. Ingest subscription and inventory data from provided CSV files
2. Calculate expected demand for each box type and size for the next 3-4 months
3. Compare demand against available and incoming inventory
4. Display shortages by box type, size, and month
5. Provide a visual representation of the shortages

## Data Files

The repository contains the following CSV files:

1. **subscriptions.csv** - Contains 1,000 subscription records with fields:

   - `subscription_id`: Unique identifier (integer)
   - `customer_id`: Customer identifier (integer)
   - `subscription_type`: SUBSMALL, SUBMEDIUM, or SUBLARGE
   - `start_date`: When the subscription started (YYYY-MM-DD)
   - `status`: Subscription status (all "active" for this exercise)
   - `selected_boxes`: JSON array of box selections in order [June, July, August, September]

2. **current_inventory.csv** - Contains current inventory levels:

   - `box_type`: Box identifier (TWN25, CZE25, etc.)
   - `size`: SMALL, MEDIUM, or LARGE
   - `quantity`: Current quantity in stock

3. **incoming_inventory.csv** - Contains expected inventory arrivals:
   - `box_type`: Box identifier
   - `size`: SMALL, MEDIUM, or LARGE
   - `quantity`: Quantity arriving
   - `arrival_date`: Date when inventory will arrive (YYYY-MM-DD)

## Business Rules

- Subscription renewals occur on the 1st of each month
- Churn rates vary by subscription type:
  - SUBSMALL: 8% monthly
  - SUBMEDIUM: 10% monthly
  - SUBLARGE: 12% monthly
- The company adds approximately 100 new subscriptions per month
- About 50% of subscribers receive the default box each month
- For inventory planning, consider June 2025 as the current month

## Technical Requirements

1. Create a web application with:

   - Backend: Python (Flask or FastAPI)
   - Frontend: JavaScript/React
   - Data processing: Python (pandas or similar libraries)

2. Your solution should include:

   - Data ingestion and processing
   - Business logic to calculate expected demand
   - A frontend dashboard displaying the shortages

3. The code should be well-organized and include:
   - Clear documentation
   - Appropriate error handling
   - Reasonable test coverage

## Deliverables

1. Source code for the full-stack application
2. Documentation explaining your approach and any assumptions
3. Instructions for running the application locally

## Evaluation Criteria

Your solution will be evaluated based on:

1. **Accuracy**: Correctly identifying shortages based on the data
2. **Assumptions**: Ability to describe any assumptions you made in your calculations
3. **Technical implementation**: Code quality, organization, and performance
4. **Full-stack skills**: Effectiveness of both backend and frontend components
5. **Data handling**: Appropriate processing and analysis of the CSV data
6. **Visualization**: Clear and informative presentation of shortage information
7. **Business understanding**: Incorporating the business rules correctly

## Getting Started

1. Clone this repository
2. Set up your development environment
3. Explore the data files to understand their structure
4. Develop your solution
5. Document your approach and any assumptions

Good luck!
