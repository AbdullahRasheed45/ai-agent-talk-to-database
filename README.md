# AI Agent: Talk to Your Database

[![Streamlit](https://img.shields.io/badge/Streamlit-FF6B35?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

## Overview

**AI Agent: Talk to Database** is an intuitive, AI-powered tool that lets you query your MySQL database using natural language. No more writing complex SQL—simply ask questions in plain English, and the agent generates, previews, executes, and explains the results for you!

Built with [Streamlit](https://streamlit.io/) for the UI, Nebius AI for natural language to SQL translation, and [LangChain](https://www.langchain.com/) for orchestration, this app is perfect for e-commerce analysts, data enthusiasts, or anyone who wants to democratize database access.

### Key Features
- **Natural Language Queries**: Convert everyday questions into accurate SQL (supports SELECT, JOINs, aggregations, filters, sorting, and limits).
- **Secure Configuration**: Sidebar setup for Nebius API key and MySQL connection string.
- **SQL Preview & Execution**: Review generated SQL before running it.
- **Interactive Results**: View query results in a responsive DataFrame with row counts.
- **AI Explanations**: Get plain-English summaries of your results.
- **Query History**: Automatically save past questions, SQL, and result summaries.
- **Example Prompts**: Built-in suggestions for e-commerce databases (e.g., products, orders, categories).
- **Modular Architecture**: Separated into UI (`app.py`), database handling (`database.py`), and AI services (`ai_services.py`).

## Prerequisites
- Python 3.8+
- A MySQL database (tested with e-commerce schemas like products, orders, categories).
- A Nebius API key for AI-powered query generation.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AbdullahRasheed45/ai-agent-talk-to-database.git
   cd ai-agent-talk-to-database
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install streamlit pandas sqlalchemy langchain openai mysql-connector-python
   ```

3. (Optional) Set up environment variables in a `.env` file:
   ```env
   NEBIUS_API_KEY=your_nebius_api_key_here
   ```

## Usage

1. Run the app:
   ```bash
   streamlit run app.py
   ```

2. In the sidebar:
   - Enter your Nebius API key.
   - Provide your MySQL connection string (format: `mysql://username:password@host:port/database`).

3. In the main area:
   - Type a question (e.g., "What are the top 5 most expensive products?").
   - Click **🚀 Generate SQL Query**.
   - Review the SQL, then click **▶️ Execute Query**.
   - Optionally, click **🤖 Explain Results** for insights.

### Example Questions
- "How many orders do we have this month?"
- "Show me products in the 'Electronics' category with prices over $100."
- "What are the total sales by category?"

## Architecture

- **UI Layer** (`app.py`): Handles Streamlit interface, user inputs, and result display.
- **Database Layer** (`database.py`): Manages MySQL connections, query execution, and error handling.
- **AI Layer** (`ai_services.py`): Integrates Nebius AI for NL-to-SQL translation and result explanations.

## Configuration

- **Nebius API**: Get your API key from Nebius AI. The app uses it to power the LLM for SQL generation.
- **Database**: Ensure your MySQL user has read permissions. The app parses the connection string automatically.

## Troubleshooting
- **API Key Error**: Verify your Nebius key is valid and set as an environment variable.
- **Connection Issues**: Check your MySQL credentials and network access.
- **Empty Results**: Ensure your database has data matching the query.

## Contributing
Contributions are welcome! Please fork the repo and submit a pull request. For major changes, open an issue first.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

**Abdullah Rasheed**
- 🌐 Portfolio: [techvibes360.com](https://techvibes360.com)
- 💼 LinkedIn: [abdullah-rasheed](https://www.linkedin.com/in/abdullahrasheed-/)
- 📧 Email: abdullahrasheed45@gmail.com

## Acknowledgments
- [Streamlit](https://streamlit.io/) for the amazing UI framework.
- [LangChain](https://www.langchain.com/) for the powerful agent patterns.

---

*Built with ❤️ by Abdullah Rasheed. Questions? Feel free to reach out!*
