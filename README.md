# Assignment 

Both assignment are complete with instructions, code explanations, dependencies in the `.ipynb` file. 
<br>Here's a list of things that each assignment holds:
> Note: This is tested only on a Linux environment.

## [Assignment 1](https://github.com/snehangsude/TensorIoT/blob/master/Assingment_1.ipynb):
- Find the item with the least rating
- Find the item with the most rating
- Find the item with the longest reviews
- Store it into a parquet file

## [Assignment 2](https://github.com/snehangsude/TensorIoT/blob/master/Assingment_2.ipynb):

- Find the item with the least rating
- Find the item with the most rating
- Find the item with the longest reviews
- Store it into a parquet file
- Ingest the data in a postgre table

### Tools/Libraries Used
- Pyspark
- Docker
- Postgres


# To run an assignment: 
Open a terminal and enter the commands below:

#### Docker installed:
```
git clone "https://github.com/snehangsude/TensorIoT.git"
cd TensorIoT
python3 -m venv .iot
source .iot/bin/activate
pip install -r requirements.txt
```
#### Docker not installed:
```
sudo snap install docker

git clone "https://github.com/snehangsude/TensorIoT.git"
cd TensorIoT
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
> Note: This needs to be run only after Assignment_2.ipynb file has been run successfully
