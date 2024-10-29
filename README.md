# SVU - Advanced Web Development (AWD) Assignment by PhD. Bassel Alkhateeb for S24

by Group assignment S24 (Issa & Loai & Mohamad & Mariam) 
MCS_AWD_S24

Live Hosting: https://Issasabagh.pythonanywhere.com  
Github Repo: https://github.com/IssaSVU/SVU-Assignment  
README.md File: https://github.com/IssaSVU/SVU-Assignment/blob/main/README.md

## Installation

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

result:


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

to make Django knows the 'templates' 



then i write StockData model into ``` stockapp/models.py ``` like this:



then i registered the model in ``` stockapp/admin.py ``` and make some configurations to show it probably in admin site:  



then i create a super user by running this command to ability to login in admin site:  

``` python ./manage.py createsuperuser ```

then i create the only view in my project to handle rendering html page and handle POST request which will be came to it from client side (JavaScript):  


then i add those lines into ``` _project/settings.py ``` to make Django knows redirect urls for login/logout:  

```
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/accounts/login'
```

### JavaScript

i wrote a script to handle sending POST request to the endpoint to get json fetched data and create some elements in page like this:


i used chartjs (cdn version) library to creating a plot which representing the data i fetched
```
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
```

i wish the project describe it self if i missing something in this report.  


Thanks for reading.

