# Book Knowledge ChatBot

## Project Overview
The **Book Knowledge ChatBot** is a web-based application that utilizes Google Cloud Run, Flask, and Dialogflow to answer book-related queries. The chatbot is trained using the Complete Works of William Shakespeare, sourced from Project Gutenberg. It provides an interactive interface for users to ask questions about Shakespeare's works.

## Deployment Details
- **Google Cloud Project ID:** cproject-436307
- **Cloud Run Service Name:** bookagent
- **Application URL:** [Book Knowledge ChatBot](https://bookagent-260842392440.us-central1.run.app/)
  

## Features
- Uses **Dialogflow CX** to process user queries and generate responses.
- Supports **text-based and voice-based interactions**.
- Stores book data in **Python lists** for simplified deployment.
- Provides a downloadable **PDF version** of Shakespeare's works via Google Cloud Storage.
- Hosted using **Google Cloud Run** for efficient deployment and scaling.

## Technology Stack
- **Backend:** Flask, Python
- **Frontend:** HTML, CSS, JavaScript
- **Chatbot AI:** Dialogflow CX
- **Cloud Services:** Google Cloud Run, Google Cloud Storage
- **Containerization:** Docker

## Application Components
1. **Frontend (User Interface)**  
   - Built using HTML, CSS, and JavaScript.
   - Displays chatbot responses and book content.

2. **Backend (Flask Application on Cloud Run)**  
   - Handles user requests and communicates with Dialogflow CX.
   - Manages API routing and response handling.

3. **Chatbot (Dialogflow CX Agent)**  
   - Processes natural language queries.
   - Retrieves responses based on book content.

4. **Storage (Google Cloud Storage)**  
   - Stores a downloadable PDF version of Shakespeare’s works.

5. **Voice Interaction (Phone Gateway)**  
   - Users can interact with the chatbot using a phone number: **+1 (470) 795-3137**

## Setup & Deployment
### Prerequisites
- Python 3.9+
- Google Cloud SDK
- Git
- Docker

### Steps to Deploy
1. **Clone the repository:**
   ```sh
   git clone https://github.com/siva-rama-krishna-reddy18/Book-Agent-chatbot.git
   cd Book-Agent-chatbot
   ```
2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
3. **Run the application locally:**
   ```sh
   python app.py
   ```
4. **Deploy to Google Cloud Run:**
   ```sh
   gcloud builds submit --tag gcr.io/cproject-436307/bookagent
   gcloud run deploy bookagent --image gcr.io/cproject-436307/bookagent --platform managed
   ```

## Architecture Overview
1. **User Interaction:** Frontend sends user input to the backend.
2. **Backend Processing:** Flask app processes the input and forwards it to Dialogflow CX.
3. **Chatbot Response:** Dialogflow determines the appropriate response and returns it to Flask.
4. **Storage Access:** If needed, Cloud Storage is queried for book-related data.
5. **User Display:** The frontend receives and presents the response.

## Examples:
- **Query Example:** "Who is the author of the book?"
  - Response: "The author of *The Complete Works of William Shakespeare* is William Shakespeare."
- **Query Example:** "What are Shakespeare’s sonnets about?"
  - Response: "Shakespeare's sonnets explore themes of love, beauty, time, and mortality.

## Lessons Learned
- **Dialogflow CX provides an efficient way to create AI-driven chatbots.**
- **Google Cloud Run simplifies deployment and management.**
- **Cost optimization is possible using free-tier services.**
- **Scalability can be improved with Firestore for larger datasets.**

## Contributors
- **Siva Rama Krishna Reddy Kunchala**
  - Email: [kunchalas2023@fau.edu](mailto:kunchalas2023@fau.edu)


