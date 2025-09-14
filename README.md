# My_LangGraph_Company_Revenue
**Summary -**
This project is a conversational assistant built using _LangGraph_ and _LangChain_. It enables users to interact with structured data (CSV files) through natural, multi-turn dialogue while preserving context across queries. The design is modular - by simply replacing the CSV file, the assistant can be adapted to answer questions in different domains, with no pre-training required.


**Setup Instructions -**
1. Clone the repository and open the notebook in Google Colab or Jupyter Notebook.
2. Provide your OpenAI API key when prompted.
3. Ensure the input CSV (company_financials_quarterly.csv) is available: During execution select: Option 1 for GitHub repo and 2 is for Google Drive
   
**Architecture & Reasoning Flow -**
1. **_Input_** - User query (multi-turn conversation supported).
2. **_Intent Processing_** - Query passed to LangGraph for orchestration.
3. **_Document Handling_** - CSV data chunked using RecursiveCharacterTextSplitter.
4. **_Embeddings & Vector Store_** - FAISS used for semantic search over CSV content.
5. **_Reasoning Flow_** – User Question → Retrieve relevant chunks → LLM reasoning via ChatOpenAI (gpt-3.5-turbo) → Response generated.


**Tools & Libraries used -**
1. Langchain and Langgraph libraries.
2. ChatOpenAI (model - _gpt-3.5-turbo_)
3. RecursiveCharacterTextSplitter (for chunking)
4. FAISS (Facebook AI Similarity Search) as Vector Database


**Files in the project -**
1. company_financials_quarterly.csv - Input dataset containing 25 years of quarterly financial data.
2. LangGraph_Company_Revenue_Model.ipynb - Main Google Colab notebook with the conversational assistant implementation.
3. execution_snapshot.png - Screenshot showing an example Q&A session with the chatbot.
4. README.md - Project documentation and usage instructions.

**Note-**
The code is tested on _Google Colab_. In the Load & Prepare Document section, an **if** condition handles whether the file is loaded from _GitHub or Google Drive._
