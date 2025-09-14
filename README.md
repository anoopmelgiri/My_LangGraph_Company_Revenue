# My_LangGraph_Company_Revenue
**Summary -**
This project is a conversational assistant built using _LangGraph_ and _LangChain_. It enables users to interact with structured data (CSV files) through natural, multi-turn dialogue while preserving context across queries. The design is modular - by simply replacing the CSV file, the assistant can be adapted to answer questions in different domains, with no pre-training required.


**Setup Insrtuctions -**
1. Clone the repository and open the notebook in Google Colab or Jupyter Notebook.
2. Provide your OpenAI API key when prompted.
3. Ensure the input CSV (company_financials_quarterly.csv) is available: Option 1 is for GitHub repo and 2 is for Google Drive
   
**Architecture & Reasoning Flow**
**_Input_** - User query (multi-turn conversation supported).
**_Intent Processing_** - Query passed to LangGraph for orchestration.
**_Document Handling_** - CSV data chunked using RecursiveCharacterTextSplitter.
**_Embeddings & Vector Store_** - FAISS used for semantic search over CSV content.
**_Reasoning Flow_** – User Question → Retrieve relevant chunks → LLM reasoning via ChatOpenAI (gpt-3.5-turbo) → Response generated.


**Tools & Libraries used -**
1. Langchain and Langgraph libraries.
2. ChatOpenAI by OpenAI, model - _gpt-3.5-turbo_
3. For Chunking - _RecursiveCharacterTextSplitter_
4. For Embeddings and Vector DB, _FAISS_ (Facebook AI Similarity Search)


**Key steps to run -**
1. Provide your _OpenAI API key_ when prompted in the notebook.

2. The input dataset is a CSV file containing 25 years of quarterly company financials.
   Columns include: _Quarter, Revenue_MillionUSD, Expenses_MillionUSD, Profit_MillionUSD, Growth_Rate, and Employees._
   You can replace this file with any other CSV - the pipeline will work the same way.

3. The code is tested on _Google Colab_. In the Load & Prepare Document section, an if condition handles whether the file is loaded from _GitHub or Google Drive._

4. A screenshot of the full execution is included to show example questions and the model’s responses.

**Files in the project -**
1. company_financials_quarterly.csv - Input dataset containing 25 years of quarterly financial data.
2. LangGraph_Company_Revenue_Model.ipynb - Main Google Colab notebook with the conversational assistant implementation.
3. execution_snapshot.png - Screenshot showing an example Q&A session with the chatbot.
4. README.md - Project documentation and usage instructions.
