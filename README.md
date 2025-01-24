# Crest Project

## **Step 1: Clone the Project
Clone the repository from GitHub:

```
git clone <repository-url>
cd crest_project
```

## **Step 2: Create a Virtual Environment
Create and activate a virtual environment:

```
python -m venv venv

For macOS/Linux:
source venv/bin/activate

For Windows:
venv\Scripts\activate
```


## **Step 3: Install Dependencies
```
pip install -r requirements.txt
```

## **Step 4: Set Up the Database
```
python manage.py makemigrations
python manage.py migrate
```

## **Step 5: Create a Superuser

```python manage.py createsuperuser
```
Then after login in to Django admin create a new user other than admin user 

## **Step 6: Run the Server:

```
python manage.py runserver
```

The server will run on http://127.0.0.1:8000/

Note: You can import the postman collection and use the api requests

## **Api

**1. Token Generation
method - POST 
url - http://127.0.0.1:8000/api/token/

json data use the super user details for admin user
example:
{
    "username": "admin",
    "access": "admin"
}

You can use New user by creating it directly from admin panel 


2.Create a Product (POST)
Endpoint: http://127.0.0.1:8000/api/products/
Request Body (form-data in Postman or JSON):

{
    "title": "Sample Product",
    "description": "Product Description",
    "price": 299.99,
    "discount": 10,
    "ssn": "123-456-789",
    "image": "test.jpg"
}

3.Retrieve Products (GET)
Endpoint: http://127.0.0.1:8000/api/products/

Example filters:

?title=Sample
?price=100
?ordering=created_on
?search=Sample

4.Update a Product (PUT/PATCH)
Endpoint: http://127.0.0.1:8000/api/products/<id>/
{
    "title": "Updated Product Title"
}


5.Delete a Product (DELETE)
Endpoint: http://127.0.0.1:8000/api/products/<id>/
(This performs a soft delete by setting is_active to False.)

6.Export Products (GET)
Endpoint: http://127.0.0.1:8000/api/export/
This will download an Excel file with all product data.
