# SVU - Advanced Web Development (AWD) Assignment by PhD. Bassel Alkhateeb for S24

by Group assignment S24 (Issa & Loai & Mohamad & Mariam) 
MCS_AWD_S24

Live Hosting: https://Issasabagh.pythonanywhere.com  
Github Repo: https://github.com/IssaSVU/SVU-Assignment  
README.md File: https://github.com/IssaSVU/SVU-Assignment/blob/main/README.md

## Installation Assignment

- ``` git clone https://github.com/IssaSVU/SVU-Assignment.git ```
- ``` cd SVU-Assignment  ```
- ``` npm install ```
- ``` pip install -r requirements.txt ```  

if you want to run the server **locally** run this command  
``` python ./manage.py runserver --insecure ```  
adding ```--insecure``` because DEBUG=False in ```settings.py```  



### HTML & CSS

I used Django templates for rendering html pages  in that structure


<!-- <img src='./assets/login.png'> -->


### Python

i wrote a Python program that uses the `yfinance` library to 
fetch real stock data from Yahoo Finance.  

i separated the logic into multiple functions like:


first function (history):
it takes ticker_symbol, start_date and end_date as arguments  
and return a list of dictionaries including fetched data.  

``` stockapp/controllers.py ```


``` python ./app.py ```


### Django

first i create an app (stockapp) with this command:  
```python ./manage.py startapp stockapp```

after that i modified the ```./_project/settings.py``` with these lines:  

```./_project/settings.py```

to make Django know the new app which i add

```
INSTALLED_APPS = [
    'stockapp', # add this
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

### JavaScript

i wrote a script to handle sending POST request to the endpoint to get json fetched data and create some elements in page :


i used chartjs (cdn version) library to creating a plot which representing the data i fetched
```
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
```


Thanks for reading.

