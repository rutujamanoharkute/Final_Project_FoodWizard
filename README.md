# Final_Project_FoodWizard
# FoodWizard
### Youtube Link: https://youtu.be/xQv5ouowBUk

### Functionalities:


#### YouTube Video Summarization with FoodWizard:

Utilizes FoodWizard, powered by OpenAI's technology, to extract content from cooking tutorials available in various languages such as Hindi, Tamil, Marathi, and English.
Recipe 

#### Recommendations:

Users can input any text, including specific instructions or preferences, and receive personalized recipe recommendations based on their input.
Recipe Filtering:

Allows users to filter and search through the listed recipes, making it easier to find recipes based on their preferences and dietary requirements.

### How to Run
1.Creating Virtual Environment
2. Create a virtual environment using the command python -m venv <name of virtual env>.
3. Install dependencies required to run the project using pip install -r path/to/requirements.txt
4. Activate created virtual env by running source <name of virtual env>/bin/activate

5.Create virtual environment and activate it
create a .env file to add the credentials required to connect with snowflake, Pinecone API Key, and OpenAI API Key. The required fields are the following

- AIRFLOW_UID=AIRFLOW_UID
- AIRFLOW_PROJ_DIR=AIRFLOW_PROJ_DIR
- SNOWFLAKE_USER = SNOWFLAKE_USER
- SNOWFLAKE_PASSWORD =SNOWFLAKE_PASSWORD
- SNOWFLAKE_ACCOUNT = SNOWFLAKE_ACCOUNT
- SQLALCHEMY_SILENCE_UBER_WARNING=1
- SNOWFLAKE_TABLE = SNOWFLAKE_TABLE
- SNOWFLAKE_TABLE_VIDEO = SNOWFLAKE_TABLE_VIDEO
- SNOWFLAKE_SCHEMA = SNOWFLAKE_SCHEMA
- SQLALCHEMY_SILENCE_UBER_WARNING=1
- SNOWFLAKE_DATABASE = SNOWFLAKE_DATABASE
- SNOWFLAKE_WAREHOUSE = SNOWFLAKE_WAREHOUSE
- PINECONE_API_KEY = PINECONE_API_KEY
- OPENAI_API_KEY = OPENAI_API_KEY
- BASE_URL = BASE_URL

3.Docker

6.How to run
```
 docker compose build
 docker compose up

```
