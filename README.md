An example of how to use FlaskAPI with database  
> I use sqlalchemy for flask
# Installation
```
  
# linux  
python3 -m venv .venv
source .venv/bin/activate  
pip install -r requirements.txt  
  
# windows  
python -m venv .venv  
.venv/Scripts/activate
pip install -r requirements.txt  
```
# RUN
create a database file for sqlalchemy  
> I use sqlitedb.db  
```
python createDB.py
python app.py
```

# GET and POST
use <https://www.postman.com/> to GET and POST  
> or  
```python
# GET
import requests  

url = "http://127.0.0.1:5000"
route = "/route"

response = requests.get( url+route )  
print(response.json())  
  
# POST
import requests  
data = {
    # your data
}
response = requests.post( url+route , json = data)   
print(response.json())  
```
  
# Create dummy data
create sqlitedb.db first
```python
python generate_dummy_data.py
```  
  
# Function
> Example  
```python
import requests

url = "http://127.0.0.1:5000"

```
## Create User
```python  
data = {
    "name": "Bob",
    "email": "bob@testing.123",
    "address": "456 Street",
    "phone": "61234567"
}
response = requests.post( url+"/user", data = data)   
print(response.json())  
```
{'message': 'User created'}  

## Get User
### All
```python
# Descending order
response = requests.get( url+"/user/descending_id")  
print(response.json())  

# Ascending order
response = requests.get( url+"/user/ascending_id")  
print(response.json())  
```
### One
```python
id = 1
response = requests.get( url+"/user/"+id )  
print(response.json())  
```

