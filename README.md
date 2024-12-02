# Dapsy 🕵️‍♂️✨
<br>
<br>


## Overview

Dapsy is a powerful web extension designed to empower users by identifying and combatting dark patterns on various websites, particularly focusing on E-commerce platforms. Ensuring users a transparent and ethical online experience.

##### About Dark Patterns => https://www.deceptive.design/

![Screenshot 2024-07-13 024617](https://github.com/user-attachments/assets/e7c2dbe5-7c9c-4759-ab72-042c90fe3b2c)


<iframe width="560" height="315" src="https://www.youtube.com/embed/1DoYa1wVWhA?si=FCnzDxHuiJs5_Q4P" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>





## Dapsy-BERT Model Scores

### Sweeps Training Hyperparametrs

<p align="center">
  <img src="https://onionreads.com/wp-content/uploads/2024/05/dapsy-bert-12sweeps.png" alt="BERT Fine-Tuned Sweep training " width="600px" />
</p>



## Project Setup Locally 🚀

### Link of Dapsy-BERT Trained Model
1. Huggingface spaces link --> https://huggingface.co/spaces/4darsh-Dev/dark_pattern_detector_app/tree/main/models

### Setting up project locally

1. clone the git repository locally.
```bash 
git clone https://github.com/sunpreetsinghsoni/Dapsy.git
```
2. Install python and setup virtual envionment. 
#### 1. Open terminal 
```bash 
pip install virtualenv 
```
```bash 
cd Dapsy
```
##### 1. For setting django-web-app
```bash 
cd django-web-app
```
##### 2. For setting django-mlapi-backend
```bash 
cd django-mlapi-backend
```
#### create a sample .env file in root directory (OPTIONAL)
```ini
#.env file


# Email server configuration
EMAIL_HOST=smtp.your-email-provider.com
EMAIL_HOST_USER=your_email@example.com
EMAIL_HOST_PASSWORD=your_email_password


# database configuration or use default sqlite3 
DB_NAME=your-database-name
DB_USER=your-db-user-name
DB_PASSWORD=your-db-password
DB_HOST=your-db-host
DB_PORT=your-db-port
PJ_SECRET_KEY=your-django-project-secret-key

```
```bash
python -m venv myenv 
```
#### Activating virtual environment named as myenv
##### 1. In Windows 🪟
```bash 
.\myenv\Scripts\activate  
```
##### 2. In Linux/Mac 🐧
```bash
 source myenv/bin/activate
 ```

3. Installing required modules and libraries
```bash
 pip install -r requirements.txt 
 ```

4. Running Django Development Server 
Do the following task for contributing to project and you have to revert these changes before committing
These steps can be used for working on local device for contribution

##### In dapsy/settings.py
```python
# for vercel deployment 
# SECRET_KEY = os.environ.get("PJ_SECRET_KEY")
SECRET_KEY="default-development-secret-key"

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

DATABASES = {
    #  setting default sqlite3 configuration for development server
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
    # for vercel deployment
    # 'default': {
    #     'ENGINE': 'django.db.backends.postgresql_psycopg2',
    #     'NAME': os.environ.get("DB_NAME"),
    #     'USER': os.environ.get("DB_USER"),
    #     'PASSWORD': os.environ.get("DB_PASSWORD"),
    #     'HOST': os.environ.get("DB_HOST"),
    #     'PORT': os.environ.get("DB_PORT"),
    # }
}
```
##### In dapsy/urls.py
```python


# # vercel deployment configuration
# urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
# urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)

```
```bash 
python manage.py makemigrations 
```
```bash 
python manage.py migrate 

```bash 
python manage.py runserver 
```
-- Server will be started at localhost (example: http://127.0.0.1:8000/)

--- Warning! - Ensure to undo the development settings changes before pushing code for vercel production and PRs.

### Setting up Dapsy Web Extension

1. Open Google Chrome Browser and visit url
``` bash
 chrome://extensions/ 
 ```
2. Turn on Developer Mode.
3. Click on load unpacked and then select the dapsy-web folder with manifest.json
4. Click on extension icon and you will find the Dapsy.
5. Open the desired website URL (https://snapdeal.com/) on web browser and then click on Analyze button.
6. The Analyzing process will start running on backend. 


## Tech Stack 🛠️

- **Web Extension:** HTML, CSS, JavaScript 
- **Python (BeautifulSoup, Scrapy):** Web scraping for price data analysis.
- **Django:** Backend for API management and Dark pattern report pattern for Dapsy
- **BERT Model:** Fine-tuned for sophisticated pattern recognition.




## Screenshots 📸

[Include screenshots of the extension interface in action.] coming soon.

## Documentation 📖

Detailed documentation on usage, contribution guidelines, and API integration can be found in the [Documentation Link](https://github.com/).



## Acknowledgments 🙏

We express our gratitude to the incredible individuals who have contributed to the development and success of Dapsy. 🌟 Your dedication, passion, and insights have played a pivotal role in shaping this project.

Special thanks to the open-source community for their continuous support and collaborative spirit. 🚀 Your contributions, whether big or small, have contributed to the growth and improvement of Dapsy.

## Feedback 📬

We value your feedback! 
Propose features, or submit pull requests. Let's create a fair and transparent digital environment together! 🌐✨


Don't forget to leave a star ⭐
Happy Coding!!❤️

<hr>

<div>
  <h2 align = "center"><img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Red%20Heart.png" width="35" height="35">Our Contributors</h2>
  <div align = "center">
 <h3>Thank you for contributing to our repository</h3>

### Show some ❤️ by starring this awesome repository!
