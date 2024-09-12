# Task2-PySpark-JSON-Example

from pyspark.sql import SparkSession

# Initialize SparkSession
spark = SparkSession.builder.appName("JSONExample").getOrCreate()

# Sample data
data = [
    {"id": 1, "name": "Alice", "age": 30},
    {"id": 2, "name": "Bob", "age": 25},
    {"id": 3, "name": "Charlie", "age": 35}
]

# Create DataFrame
df = spark.createDataFrame(data)

# Save DataFrame as JSON
df.write.json("/FileStore/tables/device1.json")
