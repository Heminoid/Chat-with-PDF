# Chat with PDF using Gemini

## Overview
This project implements a Natural Language Query Agent that answers questions based on the content of uploaded PDF files. It uses Google Generative AI for embeddings and conversational responses, FAISS for vector storage, and Streamlit for the web interface.

## Features
- Extracts text from PDF files
- Splits text into manageable chunks
- Generates embeddings using Google Generative AI
- Stores embeddings in a FAISS vector store
- Handles user queries and generates detailed answers based on the content
- Provides a Streamlit interface for easy interaction

## Running on Google Colab

1. **Open Google Colab:**
   - Go to [Google Colab](https://colab.research.google.com/)

2. **Clone the repository and open the `.ipynb` file:**
   - Clone this repository containing the `.ipynb` file.
   - Upload the `.ipynb` file to Colab and open it.

3. **Install necessary packages in Colab:**
   ```python
   !pip install streamlit
   !pip install google-generativeai
   !pip install python-dotenv
   !pip install langchain
   !pip install PyPDF2
   !pip install faiss-cpu
   !pip install langchain_google_genai
   !pip install pyngrok
   !pip install -U langchain-community
   ```

4. **Set up environment variables:**
   - In a code cell, add your Google API key:
     ```python
     import os
     os.environ["GOOGLE_API_KEY"] = "your_api_key_here"
     ```
     - Go to [Google AI Studio](https://aistudio.google.com/app/apikey)


5. **Run the Streamlit app within Colab:**
   - Use the code in the notebook to run the Streamlit app, which includes the Ngrok setup for tunneling. Make sure to replace the `your_ngrok_auth_token` with your actual Ngrok auth token.
   - Go to [Ngrok](https://dashboard.ngrok.com/)

6. **Start the Ngrok tunnel and access the app:**
   - The notebook will print a public URL provided by Ngrok. Use this URL to access the Streamlit app and interact with it.

## Running Locally

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   - Create a `.env` file in the root directory
   - Add your Google API key:
     ```plaintext
     GOOGLE_API_KEY=your_api_key_here
     ```

4. **Run the Streamlit app:**
   ```bash
   streamlit run app.py
   ``

**Ngrok not used in the case ( Access it using local env )**

## Future Improvements
- Implement conversational memory for context-aware interactions
- Enhance error handling and robustness
- Optimize storage and retrieval for scalability
- Include citation of references in responses
