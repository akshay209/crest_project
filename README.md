# Crest Project

## Step 1: Clone the Project
Clone the repository from GitHub:

```
git clone <repository-url>
cd crest_project
```

## Step 2: Create a Virtual Environment
Create and activate a virtual environment:

```
python -m venv venv

For macOS/Linux:
source venv/bin/activate

For Windows:
venv\Scripts\activate
```


## Step 3: Install Dependencies
```
pip install -r requirements.txt
```

## Step 4: Set Up the Database
```
python manage.py makemigrations
python manage.py migrate
```

## Step 5: Create a Superuser
```
python manage.py createsuperuser
```
Then after login in to Django admin create a new user other than admin user 

## Step 6: Run the Server:

```
python manage.py runserver
```

The server will run on http://127.0.0.1:8000/    

Note: You can import the postman collection and use the api requests

## Api
For admin user create super user and use it as admin    
or    
# 1. Register User
Endpoint : http://127.0.0.1:8000/api/register/    
Method - POST    
Body(Json) -     
{    
  "username": "user1",    
  "password": "password123"    
}    
    
# 2. Login Api
Endpoint : http://127.0.0.1:8000/api/login/    
Method - Post    
Body(JSON) -     
{    
  "username": "admin",    
  "password": "admin"    
}    

# 3. Create Blog
Endpoint - http://127.0.0.1:8000/api/blogs/    
Method - POST    
Headers -     
Authorization:Bearer <JWT ACCESS TOKEN>    
Content-Type:application/json    
Body(JSON)-     
{    
  "title": "New Blog test",    
  "description": "This is a new test product ",    
  "price": "250.00",    
  "discount": 15.0,    
  "ssn": "98765234321"    
}    

# 4. Read Blog
Endpoint - http://127.0.0.1:8000/api/blogs/    
Method - GET    
Headers -     
Authorization:Bearer <JWT ACCESS TOKEN>    
Content-Type:application/json    
    

# 5. Update Blog
Endpoint - http://127.0.0.1:8000/api/blogs/1/    
Method - PUT    
Headers -     
Authorization:Bearer <JWT ACCESS TOKEN>    
Content-Type:application/json    
Body(JSON)-     
{    
  "title": "Updated test",    
  "description": "This is a new test product ",    
  "price": "250.00",    
  "discount": 15.0,    
  "ssn": "98765234321"    
}    

# 6. Delete Blog
Endpoint - http://127.0.0.1:8000/api/blogs/1/    
Method - DELETE    
Headers -     
Authorization:Bearer <JWT ACCESS TOKEN>    
Content-Type:application/json    
    
# 7. Export Blog
Endpoint - http://127.0.0.1:8000/api/export-blog/    
Method - GET    
Headers -     
Authorization:Bearer <JWT ACCESS TOKEN>    
Content-Type:application/json    
    
    
