# 🤖 AI Agent: Talk to Your Database

[![Streamlit](https://img.shields.io/badge/Streamlit-FF6B35?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://www.langchain.com/)

## Overview

Transform your MySQL database into an intelligent, conversational interface! **AI Agent: Talk to Your Database** eliminates the need for complex SQL queries by allowing you to interact with your database using natural language. Simply ask questions in plain English and get instant, accurate results with AI-powered explanations.

Perfect for data analysts, business users, and anyone who wants to unlock database insights without SQL expertise.

### 🌟 Key Features

- **💬 Natural Language Interface**: Ask database questions in plain English
- **🔍 Intelligent SQL Generation**: AI converts your questions into optimized SQL queries
- **👀 Query Preview**: Review generated SQL before execution for transparency and learning
- **📊 Interactive Results**: Beautiful, responsive DataFrames with comprehensive result displays
- **🧠 AI-Powered Explanations**: Get plain-English summaries of your query results
- **📝 Query History**: Automatically tracks your questions, SQL, and results for reference
- **💡 Smart Suggestions**: Built-in example prompts for common database operations
- **🔒 Secure Configuration**: Safe API key and database credential management
- **⚡ Real-time Processing**: Instant query generation and execution

### 🎯 Perfect For

- **Data Analysts**: Query databases without writing complex SQL
- **Business Users**: Get insights from data using natural language
- **E-commerce Teams**: Analyze products, orders, and customer data effortlessly
- **Developers**: Rapidly prototype and test database queries
- **Students**: Learn SQL by seeing how natural language translates to queries

## 🏗️ Architecture

The application follows a clean, modular architecture:

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Streamlit UI  │ ──▶│   AI Services    │ ──▶│ MySQL Database │
│    (app.py)     │    │(ai_services.py)  │    │   (database.py) │
│                 │    │                  │    │                 │
│ • User Input    │    │ • NL to SQL      │    │ • Query Exec    │
│ • Results View  │    │ • Nebius AI      │    │ • Connection    │
│ • Query History │    │ • Explanations   │    │ • Error Handle  │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

**Components:**
- **UI Layer**: Streamlit interface for user interactions and result visualization
- **AI Layer**: Nebius AI integration for natural language processing and SQL generation
- **Database Layer**: MySQL connection management and query execution

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- MySQL database with sample data
- Nebius AI API key

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AbdullahRasheed45/ai-agent-talk-to-database.git
   cd ai-agent-talk-to-database
   ```

2. **Set up your environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install streamlit pandas sqlalchemy langchain openai mysql-connector-python python-dotenv
   ```

4. **Configure your environment:**
   ```bash
   # Create .env file (optional)
   echo "NEBIUS_API_KEY=your_api_key_here" > .env
   ```

### Launch the Application

```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`

## ⚙️ Configuration

### 1. API Key Setup
- Get your Nebius AI API key
- Enter it in the sidebar or set the `NEBIUS_API_KEY` environment variable

### 2. Database Connection
Enter your MySQL connection string in the sidebar:
```
mysql://username:password@host:port/database_name
```

**Example:**
```
mysql://user:password@localhost:3306/ecommerce_db
```

### 3. Database Permissions
Ensure your MySQL user has `SELECT` permissions on the target database.

## 💡 Usage Examples

### Sample Questions for E-commerce Database

**Product Analysis:**
- "What are the top 5 most expensive products?"
- "Show me products in the Electronics category under $500"
- "How many products do we have in each category?"

**Sales & Orders:**
- "What are our total sales this month?"
- "Show me the latest 10 orders with customer information"
- "Which customers have spent more than $1000?"

**Inventory Management:**
- "Which products are running low in stock?"
- "Show me products that haven't sold in the last 30 days"
- "What's our average order value by product category?"

### How It Works

1. **Ask a Question**: Type your question in natural language
2. **Generate SQL**: Click "🚀 Generate SQL Query" to see the AI-generated SQL
3. **Review & Execute**: Examine the SQL, then click "▶️ Execute Query"
4. **Get Insights**: Optionally click "🤖 Explain Results" for AI-powered analysis

## 🔧 Supported SQL Operations

- **SELECT statements** with complex filtering
- **JOINs** across multiple tables
- **Aggregations** (COUNT, SUM, AVG, MIN, MAX)
- **GROUP BY** and **HAVING** clauses
- **ORDER BY** with sorting options
- **LIMIT** for result pagination
- **Date/Time filtering** and calculations

## 🛠️ Troubleshooting

### Common Issues

**"API Key Error"**
- Verify your Nebius AI API key is correct
- Check if the key is properly set in environment variables or sidebar

**"Connection Failed"**
- Verify MySQL connection string format
- Ensure database server is running and accessible
- Check username/password credentials
- Confirm database name exists

**"Empty Results"**
- Ensure your database contains relevant data
- Try simpler questions first
- Check table names match your question context

**"SQL Generation Issues"**
- Be specific in your questions
- Use table/column names that exist in your database
- Try rephrasing complex questions into simpler ones

### Performance Tips

- **Use specific questions** for better SQL generation
- **Include relevant context** like table names when possible
- **Start with simple queries** to understand your data structure
- **Review generated SQL** to learn and improve future questions

## 🤝 Contributing

We welcome contributions to improve the AI database agent!

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and test thoroughly
4. Commit your changes: `git commit -m 'Add amazing feature'`
5. Push to your branch: `git push origin feature/amazing-feature`
6. Open a Pull Request

### Contribution Ideas

- Support for additional database types (PostgreSQL, SQLite)
- Enhanced SQL query optimization
- Better error handling and user feedback
- Query result visualization charts
- Export functionality for results
- Advanced natural language understanding

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **[Streamlit](https://streamlit.io/)** for the excellent web framework
- **[LangChain](https://www.langchain.com/)** for orchestration patterns
- **[Nebius AI](https://nebius.ai/)** for powerful language model capabilities
- **Open Source Community** for inspiration and tools

## 📞 Contact

**Muhammad Abdullah Rasheed**
- 🌐 Portfolio: [techvibes360.com](https://techvibes360.com)
- 💼 LinkedIn: [abdullah-rasheed](https://www.linkedin.com/in/abdullahrasheed-/)
- 📧 Email: abdullahrasheed45@gmail.com

---

*Built with ❤️ by Muhammad Abdullah Rasheed. Ready to make your database conversations more intelligent?*
