 📖 Setting up the Flask + MySQL Registration App

1️⃣ Prerequisites

Before starting, make sure you have:

    Python 3.10+ installed  

    pip installed

    MySQL server installed and running

    virtualenv for isolated Python environment

2️⃣ Clone or Copy the Project
    git clone <your-repo-url>
    cd webapp
    Use gitignore to ignore the files you don't want to push on github

3️⃣ Create a Virtual Environment
    python3 -m venv .venv
    source .venv/bin/activate  # Linux
 

4️⃣ Install Python Dependencies
    pip install -r requirements.txt


5️⃣ Set Up Environment Variables

Create a file .env in your project root:

DB_HOST=localhost   
DB_USER=flaskuser   
DB_PASSWORD=StrongPassword123!
DB_NAME=froshims


⚠️ Add .env to .gitignore to keep passwords secure.

6️⃣ Install and Start MySQL
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql
sudo systemctl enable mysql


Create MySQL user and grant privileges:

sudo mysql
CREATE DATABASE froshims;
CREATE USER 'flaskuser'@'localhost' IDENTIFIED BY 'StrongPassword123!';
GRANT ALL PRIVILEGES ON froshims.* TO 'flaskuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;

7️⃣ Run the Flask App
flask run


Or, if using app.py directly:

python app.py


Default host/IP: 127.0.0.1 (localhost)

Default port: 5000

Access the app in your browser:

http://127.0.0.1:5000

 

 

 
 