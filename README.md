# Freelance Management System

## Overview

Freelance Marketplace Django is a powerful platform built on Django, facilitating seamless interactions between freelancers and clients. It provides a comprehensive solution for freelance service exchanges with a focus on security, efficiency, and ease of use.

## Features

- **User Authentication**: Secure sign-up and login functionalities with password hashing and JWT tokens.
- **Service Management**: Easy-to-use interface for freelancers to list, edit, and manage their services, including pricing and descriptions.
- **Order Processing**: Smooth order management system with real-time updates on order status.
- **Payment Integration**: Secure payment gateway integration for hassle-free transactions.

### Razorpay Integration

This project utilizes Razorpay for payment gateway integration. Razorpay is a leading payment gateway provider in India, offering secure and seamless payment processing solutions.

## Installation

### Prerequisites

Before getting started, ensure you have the following prerequisites installed on your system:

- Python 3.8+
- pip (Python package installer)
- PostgreSQL

1.**Download the .Zip file from the github and open in the IDE ( i used pycharm )**
2. **Navigate to the project directory:**

```bash
cd Freelance-Marketplace-Django
```

3. **Create and activate a virtual environment:**

- On Windows:
  ```
  py -m venv env
  ```
  ```
  env\Scripts\activate
  ```
- On Unix or MacOS:
  ```
  python -m venv env
  ```
  ```
  source env/bin/activate
  ```

4. **Install dependencies:**
```
pip install -r requirements.txt
```

## Configuration
Before running the application, configure the environment variables as per your setup by creating a `.env` file in the project root with the necessary values.


### Database Configuration

In the `settings.py` file, configure the database settings according to your setup:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_database_user',
        'PASSWORD': 'your_database_password',
        'HOST': 'localhost',  # Or your PostgreSQL server's address
        'PORT': '5432',       # Default PostgreSQL port
    }
}
```

#### Razorpay Integration
For Razorpay integration, provide your Razorpay publishable and secret keys:
```
REZORPAY_PUBLISHABLE_KEY = 'your_razorpay_publishable_key'
REZORPAY_SECRET_KEY = 'your_razorpay_secret_key'
```

### Static and Media Files
Configure the settings for static and media files:
```
STATIC_URL = '/static/'
MEDIA_URL = '/media/'
```
Ensure that you have proper file permissions and directory structures set up for media file uploads.

### Additional Configuration
You may need to configure other settings based on your project's requirements, such as email configuration, security settings, and third-party API integration.


## Migrations

Before running the application, you need to apply the migrations to set up the database schema. Follow these steps:

1. **Navigate to the project directory:**

    ```bash
    cd Freelance-Marketplace-Django
    ```

2. **Activate the virtual environment (if not already activated):**

    - On Windows:
      ```bash
      env\Scripts\activate
      ```
    - On Unix or MacOS:
      ```bash
      source env/bin/activate
      ```

3. **Check for Missing Migrations (Optional):**

    It's a good practice to check if there are any new migrations that need to be created. Run the following command to generate new migrations based on model changes:

    ```bash
    python manage.py makemigrations
    ```

    This command will inspect the models and create new migration files if any changes are detected. Review the changes and migrate them if necessary.

4. **Apply Migrations:**

    Run the following command to apply migrations:

    ```bash
    python manage.py migrate
    ```

    This command will create the necessary tables in the database based on the models defined in the Django app.

5. **Create Superuser (Optional):**

    If you want to access the Django admin interface, you can create a superuser using the following command:

    ```bash
    python manage.py createsuperuser
    ```

    Follow the prompts to create a superuser account.

Now, your database schema is set up, and you're ready to run the application.



## Usage
To run the development server:

```
python manage.py runserver
```

Visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser to access the application.



## Testing
### Running Tests
To run tests for the project, use the following command:
```
python manage.py test
```

This command will execute all the test cases defined in the project and provide feedback on their success or failure.

Testing Framework
The project uses the Django testing framework for unit tests, integration tests, and functional tests. It provides a comprehensive set of tools for writing and running tests to ensure

