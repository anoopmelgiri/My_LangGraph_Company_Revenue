# My_LangGraph_Company_Revenue
**Summary -**
This project is a conversational assistant built using _LangGraph_ and LangChain. It enables users to interact with structured data (CSV files) through natural, multi-turn dialogue while preserving context across queries. The design is modular — by simply replacing the CSV file, the assistant can be adapted to answer questions in different domains, with no pre-training required.

**Tools & Libraries used -**
1. Langchain and Langgraph libraries.
2. ChatOpenAI by OpenAI, model - gpt-3.5-turbo
3. For Chunking - RecursiveCharacterTextSplitter
4. For Embeddings and Vector DB, FAISS (Facebook AI Similarity Search)

**Key steps to run -**
1. Provide your OpenAI API key when prompted in the notebook.

2. The input dataset is a CSV file containing 25 years of quarterly company financials.
   Columns include: Quarter, Revenue_MillionUSD, Expenses_MillionUSD, Profit_MillionUSD, Growth_Rate, and Employees.
   You can replace this file with any other CSV - the pipeline will work the same way.

3. The code is tested on Google Colab. In the Load & Prepare Document section, an if condition handles whether the file is loaded from GitHub or Google Drive.

4. A screenshot of the full execution is included to show example questions and the model’s responses.
