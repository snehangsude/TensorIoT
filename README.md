# Assignment 

## For detailed code explanations, Classes, Spark Session initialization instructions are added as Markdown text inside in the respective `.ipynb` files. 

<br>The **ReadMe** file consists of how to set up your environment for a successful run. For coding breakdown, open the Assignments.

<br>Here's a list of things that each assignment holds:
> Note: This is tested only on a Linux environment.

## [Assignment 1](https://github.com/snehangsude/TensorIoT/blob/master/Assingment_1.ipynb): Movies Dataset (1,697,533 reviews)
- Find the item with the least rating
- Find the item with the most rating
- Find the item with the longest reviews
- A desired dataframe operation
- Store it into a parquet file

## [Assignment 2](https://github.com/snehangsude/TensorIoT/blob/master/Assingment_2.ipynb): Books Dataset (8,898,041 reviews)

- Find the item with the least rating
- Find the item with the most rating
- Find the item with the longest reviews
- Store it into a parquet file
- Ingest the data in a postgre table

### Tools/Libraries Used
- Python
- Jupyter
- Pyspark
- Docker: Image-Postgres

`/bin` consits of a `.jar` file that allows us to connect to any external DB with the pyspark module using `jdbc`. 

# To run an assignment: 
Open a terminal and enter the commands below:

> *Assignment_1.ipynb* doesn't require docker to be installed. Only *Assignment_2.ipynb* requires Docker.

### Setup the directories

The data directory is not uploaded which is under the name `raw_lake`. <br>
It contains all the data file. The input file with the `*.json` format and the output file format with `*.parquet`<br>

> **Instructions on how to download and store can be found inside the Assignment notebook.**

#### Docker installed:
```
git clone "https://github.com/snehangsude/TensorIoT.git"
cd TensorIoT
mkdir raw_lake
python3 -m venv .iot
source .iot/bin/activate
pip install -r requirements.txt
```
#### Docker not installed:
```
sudo snap install docker

git clone "https://github.com/snehangsude/TensorIoT.git"
cd TensorIoT
mkdir raw_lake
python3 -m venv .iot
source .iot/bin/activate
pip install -r requirements.txt
```
Once the above commands are run: 

#### For VSCode: 
Execute command `code .` <br>
Open *Assignment_1.ipynb*/*Assignment_2.ipynb* & click on Run > Run all cells.


#### For Jupyter: 
Execute command `jupyter notebook` <br>
Open *Assignment_1.ipynb*/*Assignment_2.ipynb* & click on Run > Run all cells.

# Running PGCLI

Since we are storing the data into PostgreDB, we would want to query out data from the DB. Hence the env has been supported with the use of `pgcli`.
To execute pgcli shell:

```
pgcli -h localhost -u root -d books
```
> Note: This needs to be run only after Assignment_2.ipynb file has been run successfully.
> **For password prompt** use the same password provided while executing Postgre in Docker 

# Logs
Sample logs are provided here to understand the basic runs of the notebook where logging is enabled.
- Assignment_1.ipynb logs: Prefix- movies
- Assignment_2.ipynb logs: Prefix - books

> To get pyspark logs: enable 'INFO' inside the notebooks to get detailed logs. For more info view any notebook.
