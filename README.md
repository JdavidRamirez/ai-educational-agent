# Building an AI Educational Agent

This project involves the implementation of the Gemini 2.5 Flash Model as a tool to improve the analysis process, to prevent student dropouts, and to improve student attendance. 

## What does the agent do?

The agent analyzes raw performance data and automatically generates specific intervention plans based on institutional educational guidelines, which have been added in the prompt instruction.

## What is the project Workflow? 

1. Ingest: Spark reads student records from Unity Catalog.

2. Analyze: Gemini processes the data (via CSV context) using institutional risk criteria.

3. Structure: The output is forced into strict JSON and written back to a Delta Table for immediate reporting.

### Prompt
<img width="398" height="263" alt="image" src="https://github.com/user-attachments/assets/6ba18700-08ef-41b5-a473-c6798d60bda6" />

### Outcome

<img width="533" height="108" alt="image" src="https://github.com/user-attachments/assets/9a9422a8-dfd6-4c6e-9e88-57588351dea4" />

## Tools:

* Databricks (Unity Catalog): Platform for data storage, governance, and compute.
* Apache Spark (PySpark): Engine for data ingestion and distributed processing.
* Google Gemini 2.5 Flash: LLM agent for risk analysis and logic processing.
* Python (Pandas & Google GenAI SDK): Used for data serialization and API integration.
* Delta Lake: Format for storing the structured, governed output tables.

## How to Run

* Install: Add google-genai to your Databricks cluster libraries or run %pip install google-genai.
* Configure: Set your Google API Key and update the input_path variable to point to your data source.
* Run: Execute the notebook. The script will ingest data, run the AI analysis, and save the results directly to a managed Delta Table.


