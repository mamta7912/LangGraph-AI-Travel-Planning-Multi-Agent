AI Travel Planning System using LangGraph
This project is a Multi-Agent AI System built using LangGraph.

The system uses 4 AI agents that work together to plan a complete trip automatically. It implements memory using PostgreSQL and Web Interface using Streamlit. It includes Real-time API Integration.

Project Workflow:
Flight Agent searches flights
Hotel Agent searches hotels
Itinerary Agent creates travel plan
Final Agent combines everything together
PostgreSQL stores conversation memory

Step 1: Create Python Environment
Open the terminal inside the project folder and run:

	python -m venv langgraph_env3
Now activate the environment.

Step 2: Install Dependencies
Run the following command:

	pip install langgraph langchain langchain-openai langchain-groq langchain-community langchain-tavily psycopg[binary] psycopg_pool python-dotenv tavily-python requests streamlit

	pip install -U "psycopg[binary,pool]"  langgraph-checkpoint-postgres
Step 3: Install PostgreSQL
Download and install PostgreSQL: https://www.postgresql.org/download/

⚠️ Important: While installing PostgreSQL, remember:

PostgreSQL Password
Port Number
You will need them later while creating the database connection string.

Step 4: Create Database
Open PostgreSQL and run:

CREATE DATABASE langgraph_memory_demo;

Step 5: Setup .env File
Create a .env file inside the project folder.

Add the following keys:

GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key

AVIATIONSTACK_API_KEY=your_aviationstack_api_key

DATABASE_URL=postgresql://postgres:postgres@localhost:5433/langgraph_memory_demo

Step 6: Get API Keys
Get Groq API Key
https://console.groq.com

Get Tavily API Key
https://tavily.com

Get AviationStack API Key
https://aviationstack.com

Step 7: Run the Application
Run Multi-Agent System in Terminal
	python main.py
This will test the multi-agent system through the terminal.

Run Streamlit Web App
	streamlit run frontend.py
This will launch the Multi-Agent AI web application.

Example Prompt
Plan a complete 5 days Singapore trip including flights, hotels and sightseeing under 2 lakhs.
