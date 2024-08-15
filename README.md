

# FoodWizard

**YouTube Video Summarization and Recipe Recommendation System**

### Overview

FoodWizard is an innovative application designed to streamline the process of discovering, summarizing, and recommending recipes from YouTube cooking tutorials. By leveraging the power of OpenAI's technology, including Whisper and GPT-4 Turbo, FoodWizard can process video content in multiple languages, offering English summaries and personalized recipe recommendations based on user inputs.

### YouTube Demo

Watch the demo: [YouTube Link]([https://youtu.be/xQv5ouowBUk](https://youtu.be/3NYWL_UbS0g))

### GitHub Repository

Access the full code base, setup instructions, and detailed documentation for the FoodWizard project here: [GitHub Repository Link](#).

### Features

- **YouTube Video Summarization**:
  - Extracts and summarizes content from cooking tutorials available in various languages such as Hindi, Tamil, Marathi, and English.
  - Converts the extracted content into concise English summaries for easy understanding.

- **Recipe Recommendations**:
  - Users can input specific instructions, preferences, or ingredients, and FoodWizard will provide personalized recipe recommendations tailored to their needs.

- **Recipe Filtering**:
  - Enables users to filter and search through the listed recipes based on their preferences and dietary requirements, making it easier to find suitable recipes.

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
