Name:  Rutuja Manohar Kute 
NUID: 002711730
EMAIl: kute.r@northeastern.edu
LinkedIn : https://www.linkedin.com/in/rutuja-kute/
# YouTube Demo

Watch the demo: https://youtu.be/3NYWL_UbS0g

# FoodWizardApp
A culinary companion empowered by AI to elevate your cooking with top-notch recipe
<img width="1061" alt="image" src="https://github.com/FoodWizards/FoodWizardApp/assets/114360071/d27fe38d-fc4e-43e9-bda1-8a3e5d1ab265">

### Project Overview:
### Scope:

FoodWizard is a platform designed to simplify recipe discovery and recommendation. It offers two key functionalities: YouTube video summarization and personalized recipe recommendations based on user preferences.


### Functionalities:

1. **YouTube Video Summarization with FoodWizard**: 
   - Utilizes FoodWizard, powered by OpenAI's technology, to extract content from cooking tutorials available in various languages such as Hindi, Tamil, Marathi, and English.

2. **Recipe Recommendations**: 
   - Users can input any text, including specific instructions or preferences, and receive personalized recipe recommendations based on their input.

3. **Recipe Filtering**: 
   - Allows users to filter and search through the listed recipes, making it easier to find recipes based on their preferences and dietary requirements.



### Stakeholders:
The end users for FoodWizard include:
Cooking enthusiasts seeking recipe inspiration and guidance.
Individuals with dietary restrictions or specific flavor preferences looking for tailored recipe recommendations.
Those interested in leveraging technology to simplify their culinary journey and explore new dishes.

### CodeLab: https://codelabs-preview.appspot.com/?file_id=1T4FIak6iigOSCrGLP44bsKpyt_S_kZ1uKInPsoNiBUM#0

### Architecture Diagram:



### Methodology: 


**User authenticates with Google Sign-in:** The user clicks on the Google Sign-in button on the Chrome extension. This redirects the user to a Google authorization page where they can sign in with their Google account.

**User enters Youtube URL:** Once the user has successfully signed in with Google, they can then enter a Youtube URL into the App.



** Youtube URL is to backend server:** Youtube URL is to the backend server built with FastAPI.

**FastAPI server saves Youtube URL to Snowflake database:** The FastAPI server receives the Youtube URL from the Chrome extension. The FastAPI server then connects to the Snowflake database and saves the Youtube URL for the specific user who is currently signed in.






### Project Architecture

FoodWizard consists of several key components:

1. **User Input**: Users input YouTube URLs of cooking tutorials.
2. **Summarization**: The system uses OpenAI Whisper and GPT-4 Turbo to summarize the video content.
3. **Recommendation System**: Based on the summarized content and user input, the system provides personalized recipe recommendations.
4. **User Interface**: Built using Streamlit for a user-friendly experience.

### Technologies Used

- **Backend**: FastAPI, OpenAI Whisper, GPT-4 Turbo
- **Frontend**: Streamlit
- **Containerization**: Docker
- **Data Storage**: Snowflake, Pinecone
- **Cloud Deployment**: Google Cloud Platform (GCP)

### Project Structure

 ```
├── FoodWizardApp-patch-patch-fix
│   ├── ChromeExtension
│   │   ├── background.js
│   │   ├── manifest.json
│   │   ├── obj-128x128.png
│   │   ├── obj-16x16.png
│   │   ├── obj-32x32.png
│   │   ├── obj-48x48.png
│   │   ├── options.html
│   │   ├── popup-script.js
│   │   ├── popup-signed-in-script.js
│   │   ├── popup-signed-in.html
│   │   └── popup.html
│   ├── Dockerfile
│   ├── FoodDataEDA.ipynb
│   ├── LICENSE
│   ├── README.md
│   ├── airflow
│   │   ├── airflow.cfg
│   │   ├── dags
│   │   │   ├── constants.py
│   │   │   ├── tasks
│   │   │   └── workflowdags.py
│   │   ├── foodscrapper
│   │   │   ├── foodscrapper
│   │   │   └── scrapy.cfg
│   │   └── logs
│   │       └── scheduler
│   ├── backend
│   │   ├── consumer.py
│   │   ├── database.py
│   │   ├── main.py
│   │   ├── queryvectordb.py
│   │   └── script.sh
│   ├── data.jsonl
│   ├── docker-compose.yaml
│   ├── dockerfiles
│   │   ├── backend.Dockerfile
│   │   └── frontend.Dockerfile
│   ├── fine-tune-model.ipynb
│   ├── frontend
│   │   ├── Home.py
│   │   ├── auth.py
│   │   ├── database.py
│   │   ├── naviagation
│   │   │   ├── favorite_recipe.py
│   │   │   ├── find_recipe.py
│   │   │   ├── my_info.py
│   │   │   ├── search_recipe.py
│   │   │   └── video_url_processor.py
│   │   └── ui.py
│   ├── kafka_python-2.0.3.dev0-py2.py3-none-any.whl
│   ├── messagequeue
│   │   └── kafka-ui
│   │       └── config.yml
│   ├── nginx.conf
│   └── requirements.txt
├── README.md
└── RecipeMaster_Presentation.pdf
 ```


### Data Collection and Preprocessing

- **Data Sources**: YouTube cooking videos and scraped recipes from Kaggle and other websites.
- **Preprocessing**: Whisper converts speech to text, and additional cleaning and validation are performed to ensure high-quality input for the recommendation system.

### Performance Metrics

- **Key Metrics**:
  - Accuracy of video summarization.
  - Relevance and personalization of recipe recommendations.
- **Methods**:
  - User feedback surveys.
  - Comparison with original video content.
- **Results**:
  - Preliminary tests indicate high accuracy in summarization and relevant recommendations.

### How to Run the Project

#### 1. Creating a Virtual Environment

- Create a virtual environment using the command:
  ```bash
  python -m venv <name_of_virtual_env>
  ```
- Install the necessary dependencies by running:
  ```bash
  pip install -r path/to/requirements.txt
  ```
- Activate the created virtual environment:
  ```bash
  source <name_of_virtual_env>/bin/activate
  ```

#### 2. Setting Up Environment Variables

- Create a `.env` file to add the credentials required to connect with Snowflake, Pinecone API Key, and OpenAI API Key. Include the following fields:

  ```env
  AIRFLOW_UID=AIRFLOW_UID
  AIRFLOW_PROJ_DIR=AIRFLOW_PROJ_DIR
  SNOWFLAKE_USER=SNOWFLAKE_USER
  SNOWFLAKE_PASSWORD=SNOWFLAKE_PASSWORD
  SNOWFLAKE_ACCOUNT=SNOWFLAKE_ACCOUNT
  SNOWFLAKE_TABLE=SNOWFLAKE_TABLE
  SNOWFLAKE_TABLE_VIDEO=SNOWFLAKE_TABLE_VIDEO
  SNOWFLAKE_SCHEMA=SNOWFLAKE_SCHEMA
  SQLALCHEMY_SILENCE_UBER_WARNING=1
  SNOWFLAKE_DATABASE=SNOWFLAKE_DATABASE
  SNOWFLAKE_WAREHOUSE=SNOWFLAKE_WAREHOUSE
  PINECONE_API_KEY=PINECONE_API_KEY
  OPENAI_API_KEY=OPENAI_API_KEY
  BASE_URL=BASE_URL
  ```

#### 3. Running with Docker on GCP

- Build the Docker container:
  ```bash
  docker compose build
  ```
- Deploy the application on Google Cloud Platform:
  ```bash
  docker compose up
  ```
- Ensure all required services are properly set up on GCP, such as the connection to Snowflake, Pinecone, and OpenAI APIs.

### Project Documentation

A comprehensive PDF document detailing the project is included in the GitHub repository. The document covers:

- **Introduction**: Overview of the project and its objectives.
- **Use Case**: Detailed explanation of how FoodWizard leverages generative AI, Retrieval-Augmented Generation (RAG), Large Language Models (LLMs), and LangChain.
- **Key Features**: Description of the main functionalities of the application.
- **Challenges and Solutions**: Discussion of the challenges faced during development and how they were overcome.
- **Conclusion and Future Scope**: Summary of the project's impact and potential future enhancements.

### Deployment Plan

- **Google Cloud Platform**: The project has been fully deployed on GCP using Docker for containerization. The instructions above guide you through setting up and running the application on your local machine or deploying it on GCP.

### Future Work

- **Language Support**: Expansion to support more languages.
- **Platform Expansion**: Extending the scope to other platforms beyond YouTube.
- **Long-term Vision**: Evolve FoodWizard into a comprehensive, user-friendly recipe management tool with continuous updates and community engagement.

### Conclusion

FoodWizard is designed to revolutionize how users interact with cooking content, making it more accessible and personalized. By summarizing multilingual cooking tutorials and providing personalized recipe recommendations, FoodWizard simplifies the process of discovering and managing recipes, aligning with modern AI and app development trends.

---

Make sure to replace the placeholder for the GitHub repository link with the actual link once you have it.
