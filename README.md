# My_LangGraph_Company_Revenue
This project is a conversational assistant built using LangGraph &amp; LangChain. It allows users to interact with structured data (CSV file) through natural, multiturn dialogue while preserving context across queries. The design is modular by simply replacing the CSV file or the LLM model, the assistant can be adapted to answer Qs in different domains

I have used the below mentioned tools and libraries in the project
1. Langchain and Langgraph libraries.
2. ChatOpenAI by OpenAI, model - gpt-3.5-turbo
3. For Chunking - RecursiveCharacterTextSplitter
4. For Embeddings and Vector DB, FAISS (Facebook AI Similarity Search)

Steps to run-
1. API key should be provided when asked for input

2. Input file used is from the internet, which contains quarterly data of last 25 years 
   It contains columns - Quarter Revenue_MillionUSD Expenses_MillionUSD Profit_MillionUSD Growth_Rate Employees
   This can be replaced with any other CSV, the code will work exactly the same.

3. 
