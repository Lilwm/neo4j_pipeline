# neo4j_pipeline

This data pipeline extracts data from a Neo4j graph database, transforms it using Pandas, and loads it into a Postgres relational database.

# Setup
To set up and run this data pipeline, follow these steps:

1. Clone the repository to your local machine.
2. Create a virtual environment for the project and activate it.
3. Install the required Python packages using the command pip install -r requirements.txt.
4. Open the config.py file and edit the Neo4j and Postgres connection details to match your own database credentials.
5. Run the command ` python main.py `to start the data pipeline.

# Data Schema
The data schema for this data pipeline includes the following fields:

* Customer ID (integer)
* Subscription ID (integer)
* Service ID (integer)
* Start date of subscription (date)
* End date of subscription (date)
* Price of subscription (float)

# Transformations
The data is transformed using the Pandas library. The following transformations are performed on the data:

- The date fields are converted from strings to datetime objects using the` pd.to_datetime method`.
- Any rows with null values are removed from the dataset using the `dropna` method.
- Finally, the data is loaded into a Postgres database using the psycopg2 Python library.
# Conclusion
This data pipeline provides a simple solution for extracting data from a Neo4j graph database, transforming it using Pandas, and loading it into a Postgres relational database. By following the setup instructions, you can easily set up and run the data pipeline on your own system.
