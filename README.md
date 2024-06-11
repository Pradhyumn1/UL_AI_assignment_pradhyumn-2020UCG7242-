# Online Bootcamp FAQ Chatbot with Knowledge Base

This project builds a chatbot to answer frequently asked questions (FAQs) about an online bootcamp. It leverages a small knowledge base, natural language understanding (NLU), and natural language generation (NLG) to provide informative and relevant responses to user queries.

## Key Features:

Natural Language Understanding: The chatbot comprehends user questions posed in everyday language.
Knowledge Base Integration: A curated FAQ dataset powers the chatbot's responses.
Information Retrieval: The chatbot efficiently fetches relevant information from the knowledge base.
Contextual Responses: Responses are tailored to the specific user question and context.
Fallback Mechanism: Gracefully handles questions outside the scope of the knowledge base.

### Project Structure:

data_trainer.py: Script to create and manage the knowledge base vector store.
app.py: Streamlit application for the chatbot interface.
faq_data.csv: CSV file containing the frequently asked questions and their corresponding answers. (You'll need to create this)
faiss_index: (Directory) Stores the FAISS vector database for efficient information retrieval.

Installation and Setup:

#### Clone the Repository:

git clone https://your-repository-url.git
cd your-repository-name

#### Install Dependencies:

pip install -r requirements.txt
(Make sure to create a requirements.txt file listing: streamlit, langchain, python-dotenv, chardet, huggingface_hub, sentence_transformers, faiss-cpu, google-generativeai)

#### Set Up Environment Variables:

Create a .env file in the project root directory.
Add your Google API key:
GOOGLE_API_KEY=your_actual_api_key

### How to Use:

Prepare your knowledge base:

Create a CSV file named faq_data.csv with two columns: prompt (question) and response (answer).
Run the Streamlit App:

Create a local vector database:
python data_trainer.py
Launch the app:
streamlit run app.py
Ask your questions in the chat interface.

### Important Notes:

The current implementation is designed for a small knowledge base. For larger datasets, consider using a more scalable vector database solution.
You can extend the chatbot's capabilities by adding more FAQs to faq_data.csv and retraining the vector database.

#### Example Interaction:

User: I have no experience with coding. Can I still join the bootcamp?
Chatbot: Yes, this is the perfect course for anyone who has never worked on ...

