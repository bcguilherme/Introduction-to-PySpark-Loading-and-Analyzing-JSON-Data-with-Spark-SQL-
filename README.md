# Introduction-to-PySpark-Loading-and-Analyzing-JSON-Data-with-Spark-SQL-

Introduction

This project demonstrates the basics of using PySpark to load and analyze JSON data. The dataset used in this example represents financial transactions with various attributes such as transaction ID, value, sender, recipient, transaction date, and a key for PIX transactions.

Getting Started

Prerequisites
Python 3.x
PySpark
ngrok (for Spark UI visualization)
Installation
bash
Copy code
pip install pyspark
Download ngrok:

bash
Copy code
wget -qnc https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
unzip -n -q ngrok-stable-linux-amd64.zip
Usage
Run the Jupyter notebook or script to execute the PySpark code.
Access the Spark UI using ngrok for monitoring and debugging.
bash
Copy code
./ngrok authtoken YOUR_NGROK_AUTH_TOKEN
./ngrok http 4050 &
sleep 10
curl -s http://localhost:4040/api/tunnels | grep -Po 'public_url":"(?=https)\K[^"]*'
Example Data

The dataset consists of financial transactions in JSON format:

json
Copy code
{
    "id_transacao": 1000,
    "valor": "58931.97",
    "remetente": {"nome": "Jonathan Gonsalves", "banco": "BTG", "tipo": "PF"},
    "destinatario": {"nome": "Emanuella Moura", "banco": "Itau", "tipo": "PJ"},
    "transaction_date": "2021-06-02",
    "chave_pix": "aleatoria",
    "fraude": "1"
}
PySpark Processing

JSON data is loaded into PySpark DataFrames with a defined schema.
Basic analysis, such as selecting specific columns, is demonstrated.
The processed data is saved as Parquet files for optimized storage.
License

This project is licensed under the MIT License.
