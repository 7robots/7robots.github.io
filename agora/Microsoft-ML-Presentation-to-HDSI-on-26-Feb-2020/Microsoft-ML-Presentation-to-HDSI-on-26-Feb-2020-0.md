# Microsoft-ML-Presentation-to-HDSI-on-26-Feb-2020-0

# Microsoft-ML-Presentation-to-HDSI-on-26-Feb-2020-0-HDSI_Lazzeri

**Useful Resources:**

@frlazzeri

✔AzureML GitHub:

✔Algorithm Cheat Sheet:

✔Deep Learning VS Machine Learning: ✔Automated Machine Learning Documentation:

✔Model Interpretability with Azure ML Service: ✔Azure Machine Learning Service:

✔Azure Machine Learning Designer:

✔Get started with Azure ML:

✔Azure Notebooks:

@frlazzeri

?

idea reality

@frlazzeri

idea custom ML reality

@frlazzeri

data experiment

model deploy

idea reality

There are many jobs & tools involved in production ML @frlazzeri

Azure Machine Learning

GitHub

TensorFlow, PyTorch, sklearn

Data Scientist Azure Compute – CPU/GPU/FPGA

IT / Ops Data Analyst Business Owner & many more…

Azure DevOps

Azure Data Lake GitHub

Azure Data Factory Azure Kubernetes Service

Data Engineer Azure DataBricks Azure SQL Azure IoT Edge Azure Monitor ML Engineer

**E2E Machine Learnin process**

@frlazzeri

**Train Model** Data Scientist

**Prepare Data** Data Catalog Featurize Train Evaluate register

Model

Registry

Data Engineer

**Release Model** release

Data Lake

Package Validate Profile Approve Deploy

collect

ML Engineer

**The Machine Learning Process**

@frlazzeri

@frlazzeri

Balancing capital investment constraints or objectives and service-level goals over a large assortment of stock-keeping units (SKUs) while taking demand and supply volatility into account.

**Store 1@frlazzeriInventory Optimization** **Store 2**

@frlazzeri

**Business Understanding**

✔**Ask the right questions**

✔**Define Performance Metrics**

✔**Understand what to do with your data**

**Understand what to do with your data aka.ms/AlgorithmCheatSheet**

**Business Understanding**

@frlazzeri

**Inventory**

**optimization෍ො** **Ask the right questions** What are the forecasted sales quantities per item per store for

Demand plans the next 4 weeks?

Forecasts

Sales history

Trends Using forecasting models such as determining reorder points

Local events/weather patterns and economic order quantities can help ensure optimal inventory control.

**Define Performance** Evaluation metric: MAPE

**inventory, ordering Data-driven stock, Metrics**

Predict inventory positions and

distribution

Fraud detection

Market basket analysis

**Omni-channel**

**shopping experience with machine learning**

**Understand what to do** Regression – Time Series Forecasting approach

**with your data**

@frlazzeri

**Data Acquisition & Understanding**

✔**Data Architecture**

✔**Data preprocessing**

✔**Feature Engineering**

**POS data**

**Stores**

Information about the 45 stores, indicating the type and size of store

**Features**

Contains additional data related to the store, department, and regional

activity for the given dates.

- Store - the store number

• Date - the week

• Temperature - average temperature in the region

• Fuel_Price - cost of fuel in the region

• MarkDown1-5 - anonymized data related to promotional markdowns.

- RDPI - Real Disposable Personal Income• Unemployment - the unemployment rate

**Sales**

Historical weekly sales data, which covers 3 years:

• Store - the store number

• Dept - the department number

• Date - the week

• Weekly_Sales - sales for the given department in the given store

---

@frlazzeri

**Inventory**

**ForecastingLoad results**

**ordering system**

**POS data** **Data Lake** **Azure Synapse**

**Storage Analytics**

**Power BI**

**Step 1 Step 2** **Step 3**

**Build and train Package and deploy** **MonitorInventory management architecture**

**Azure Machine Learning**

**Find Features and Process DataGather external data to improve model performanceAdd future dates to dataset to get prediction@frlazzeri**

**Starting Dataset•Get store id, item id, time, and quantities of items sold•Validate there is data for at least a year•Fill in missing gaps in data Find and Validate Data**

**Resulting DatasetAdd external data to improve model performance Add RDPI Index to data**

**Feature Engineering: Create Data Features**

Date and Time features: year, month, week of month, etc.

Season/Holiday features: New Year, U.S. Labor Day, U.S.

Black Friday, and Christmas

Fourier features to capture seasonality

Lag features: these are values at prior time steps (weeks)@frlazzeri

@frlazzeri

**Demo**

We are using C# but you can do these steps in any language!

aka.ms/AIML30

**Process Data: Add Weeks to PredictAdd default values for the number of weeks to predict to the forecasting data collection.@frlazzeri**

**C#**

**Create Time Features: Extract Concept of Time**

Date and Time features: year, month, week of month, etc.@frlazzeri

**C#**

**Create Holiday Features: Extract Holidays from Time**

Season/Holiday features: New Year, U.S. Labor Day, U.S. Black Friday, and Christmas.@frlazzeri

**C#**

**Create Fourier Features: Capture Up/Down Pattern**

Fourier features to capture seasonality@frlazzeri

**C#**

**Create Lag Features: Capture Prior Weeks to Current**

Lag features: these are values at prior time steps@frlazzeri

**C#**

**Resulting Dataset:@frlazzeri**

**Resulting Dataset:@frlazzeri**

@frlazzeri

**Modeling**

Selecting the “Right” Algorithm to Train Your Model

aka.ms/AIML30

**Azure Machine LearningAssets: Datasets, Experiments, ML Workflow Pipelines, Models, DeploymentsManagement: Compute, Datastores, Workspaces@frlazzeri**

@frlazzeri

**Deploying**

Operationalize Your Model

**Deployment with Azure Machine Learning**

**Demo: Build, Test and Deploy Your Model@frlazzeri**

**The Machine Learning Process**

@frlazzeri

**Useful Resources:**

@frlazzeri

✔AzureML GitHub:

✔Algorithm Cheat Sheet:

✔Deep Learning VS Machine Learning: ✔Automated Machine Learning Documentation:

✔Model Interpretability with Azure ML Service: ✔Azure Machine Learning Service:

✔Azure Machine Learning Designer:

✔Get started with Azure ML:

✔Azure Notebooks:

**Coming next…**

@frlazzeri

ODSC East • Boston

April 16th, 2020 • 14:00 PM Boston Hynes • Convention Center

**Training and Operationalizing Interpretable Machine Learning Models**