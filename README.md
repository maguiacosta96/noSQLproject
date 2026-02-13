# noSQLproject
# Neo4j Graph Modeling and MongoDB Data Processing with Python

## 📌 Project Overview
This project demonstrates the complete workflow of data preparation and transformation using both MongoDB and Neo4j.

The process includes cleaning and structuring a dataset stored in MongoDB, followed by modeling and loading the transformed data into Neo4j to build a graph-based representation.

## 🔄 Data Processing (MongoDB)

In MongoDB, the following tasks were performed:

- Data exploration and filtering
- Identification and handling of `NaN` values
- Cleaning inconsistent text fields (e.g., extra spaces in neighborhood names)
- Exclusion of invalid placeholder values (e.g., "VALOR NULO EN ORIGEN")
- Creation of indexes to improve query performance
- Aggregation queries to analyze and validate the dataset

This stage ensured data consistency before graph modeling.

## 🧩 Graph Model (Neo4j)

After cleaning and preparing the data, a graph model was designed and implemented in Neo4j.

### Nodes:
- Local
- Barrio
- Distrito
- Actividad

### Relationships:
- (Local)-[:UBICADO_EN]->(Barrio)
- (Barrio)-[:PERTENECE_A]->(Distrito)
- (Local)-[:REALIZA]->(Actividad)

To prevent duplication, Cypher `MERGE` statements were used when creating nodes and relationships.

## 🛠 Technologies Used
- Python
- Pandas
- MongoDB
- Neo4j
- Cypher

## 📂 Files
- `notebook_name.ipynb`: Full development process including MongoDB queries, data cleaning, and Neo4j graph loading.

## 🎯 Objective
To demonstrate the integration of document-based and graph-based databases within a single workflow, highlighting data cleaning, indexing, modeling, and relational analysis using graph structures.
