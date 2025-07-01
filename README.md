**Overview**
An ETL (Extract, Transform, Load) pipeline is used in this project to obtain regional air quality data from the Open Bristol Data Service API, preprocess and normalise the data, and store it in a local PostgreSQL database as well as a CSV file.  It is a reusable and modular pipeline.

**Features**
1. Data extraction from a GeoJSON API with error handling
2. Data is also normalized for the geographical co-ordinates which contains negative and positive values. To prepare the coordinates for potential machine learning use, latitude and longitude values are normalized to a 0–1 range using min-max normalization. This ensures equal scaling and prevents any single coordinate from dominating the model due to scale differences. The normalization is applied to each coordinate across all records after extraction.
3. Data is also loaded into CSV and PostgreSQL database
4. Well-documented, commented and modular python code.


**Tools and Technology used**
I am using Docker to run PostgreSQL, which simplifies installation and ensures a consistent, isolated environment without native setup issues on Windows. The PostgreSQL container runs on port 5432 with a set password, allowing easy connection from Python using libraries like sqlalchemy and pg8000. This setup enables efficient data operations, such as loading Pandas DataFrames into the database, streamlining development and deployment.

**Licensing**
Contains public sector information licensed under the Open Government Licence v3.0.

**Proof Of Work**
![POW](https://github.com/user-attachments/assets/0569eb31-e272-46de-b0f9-793462c4d20e)

