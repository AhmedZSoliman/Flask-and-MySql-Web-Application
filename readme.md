📖 Flask + MySQL Registration App Setup
1️⃣ Prerequisites

Before you begin, make sure you have:

Python 3.10 or higher

pip installed

MySQL Server installed and running

virtualenv (recommended for isolated environments)

2️⃣ Clone the Project
git clone <your-repo-url>
cd webapp


Make sure to configure your .gitignore file to exclude sensitive or unnecessary files (like .env and .venv).

3️⃣ Create and Activate a Virtual Environment
python3 -m venv .venv
source .venv/bin/activate  # On Linux/macOS


(On Windows: .venv\Scripts\activate)

4️⃣ Install Dependencies
pip install -r requirements.txt

5️⃣ Configure Environment Variables

Create a .env file in the project root directory:

DB_HOST=localhost
DB_USER=flaskuser
DB_PASSWORD=StrongPassword123!
DB_NAME=froshims


⚠️ Make sure .env is added to your .gitignore file to keep credentials secure.

6️⃣ Install and Configure MySQL

If MySQL is not installed:

sudo apt update
sudo apt install mysql-server


Start and enable the MySQL service:

sudo systemctl start mysql
sudo systemctl enable mysql


Now create the database and user:

sudo mysql


Inside the MySQL prompt:

CREATE DATABASE froshims;
CREATE USER 'flaskuser'@'localhost' IDENTIFIED BY 'StrongPassword123!';
GRANT ALL PRIVILEGES ON froshims.* TO 'flaskuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;

7️⃣ Run the Application
flask run


Or:

python app.py


The app will run by default on:

http://127.0.0.1:5000


Open it in your browser to access the application.
