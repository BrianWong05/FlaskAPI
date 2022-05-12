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
response = requests.get("http://127.0.0.1:5000/route")  
print(response.json())  
  
# POST
import requests  
data = {
    # your data
}
response = requests.post("http://127.0.0.1:5000/route", json = data)   
print(response.json())  
```
  
# Create dummy data
create sqlitedb.db first
```python
python generate_dummy_data.py
```  
  
# Function
## Create User
> Example  
```python
import requests  
data = {
    "name": "Bob",
    "email": "bob@testing.123",
    "address": "456 Street",
    "phone": "61234567"
}
response = requests.post("127.0.0.1:5000/user", data = data)   
print(response.json())  
```
{'message': 'User created'}

