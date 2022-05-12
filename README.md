An example of how to use FlaskAPI with database  
> I use sqlalchemy for flask
# Installation
```
python3 -m venv .venv  
source .venv/bin/activate  
```
# RUN
create a database file for sqlalchemy  
> I use sqlitedb.db  
```
touch sqlitedb.db  
python app.py
```

# GET and POST
use <https://www.postman.com/> to GET and POST  
> or
```python
# GET
import requests  
response = requests.get("127.0.0.1:5000/")  
print(response.json())  
  
# POST
import requests  
data = {
    # your data
}
response = requests.post("127.0.0.1:5000/", data = data)   
print(response.json())  
```