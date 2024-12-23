# RAG-Powered-Game-Instruction-Assistant
This project demonstrates the implementation of Retrieval-Augmented Generation (RAG) using Langchain and Chroma DB, specifically utilizing game instruction documents from the popular board game Monopoly. The aim is to create an AI-driven application that can interact with large volumes of text data, making it useful for scenarios such as building a customer support chatbot or querying extensive text datasets.

## Steps to Implement RAG (Retrieval-Augmented Generation)

### 1. **Prepare the Data**
   - Choose your data source (e.g., documents, books, lectures).
   - Place all files in a data directory.
   - Load data using `DirectoryLoader` from Langchain, converting each file into a `Document`.
   - Optionally, add metadata to each document.
   - If necessary, split the data into smaller chunks using `RecursiveCharacterTextSplitter`.

### 2. **Create Chroma DB (Store the Data)**
   - Utilize Chroma DB, an open-source AI application database that uses vector embeddings as keys.
   - Convert your data chunks into embeddings and store them in Chroma DB.

### 3. **Update Data**
   - Assign a unique ID to each data chunk based on the file path, page number, and chunk number.
   - Use this ID to check if a chunk already exists in the database or add new chunks.
   - Populate the database by running the script:
     ```bash
     python populate_database.py
     ```

### 4. **Run the RAG Application Locally**
   - Test the RAG application by running the following command:
     ```bash
     python query_data.py "Enter your prompt here"
     ```
