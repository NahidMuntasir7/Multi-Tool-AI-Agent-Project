# 🏥 Multi-tool Medical AI Agent with Multi-Database Query and Web Search Integration

An intelligent AI agent that uses multiple tools to answer medical questions by querying multiple databases converted from CSV files (Heart Disease, Cancer, Diabetes) and performs web searches for general medical knowledge.

## 📋 Features

- **Multi-Database Querying**: Implement a natural-language query system capable of retrieving information from three medical databases that have been converted from CSV formats.
  - Heart Disease dataset
  - Cancer dataset
  - Diabetes dataset
- **Web Search Integration**: Get up-to-date medical information using Tavily API
- **Automatic Tool Selection**: AI agent automatically chooses the right tool for your question
- **SQL Generation**: LLM generates SQL queries from natural language


## 🛠️ Tech Stack

- **LangGraph** - Agent orchestration
- **LangChain** - LLM framework
- **OpenAI GPT-4.1-mini** - Large Language model (via GitHub Models)
- **Tavily API** - Web search
- **Pandas** - CSV handling
- **SQLAlchemy** - Database ORM

## 📁 Project Structure

```
medical-ai-agent/
├── data/
│   ├── heart.csv           # Heart disease dataset
│   ├── cancer.csv          # Cancer dataset
│   ├── diabetes.csv        # Diabetes dataset
│   ├── heart_disease.db    # (will be generated)
│   ├── cancer.db           # (will be generated)
│   └── diabetes.db         # (will be generated)
├── notebooks/
│   └── notebook_medical_agent.ipynb     # Main 
├── requirements.txt        # Python dependencies
├── .env                    # API keys (create this)
├── .gitignore
└── README.md
```

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/NahidMuntasir7/Multi-Tool-AI-Agent-Project.git
cd Multi-Tool-AI-Agent-Project
```

### 2. Create Virtual Environment

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Mac/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Get API Keys

#### GitHub Token (for GPT-4.1-mini):
1. Go to [GitHub Models](https://github.com/marketplace/models)
2. Sign in and generate a Personal Access Token (classic)
3. Copy the token (starts with `ghp_`)

#### Tavily API Key (for web search):
1. Go to [Tavily](https://tavily.com)
2. Sign up for free account (1000 searches/month)
3. Copy your API key (starts with `tvly_`)

### 5. Create `.env` File

Create a file named `.env` in the project root:

```env
GITHUB_TOKEN=ghp_your_actual_github_token_here
TAVILY_API_KEY=tvly_your_actual_tavily_key_here
```

### 6. Add Datasets

Download the datasets and place them in the `data/` folder:

- `heart.csv` - Heart disease dataset
- `cancer.csv` - Cancer dataset  
- `diabetes.csv` - Diabetes dataset

**Dataset Sources:**
- [Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
- [Cancer Dataset](https://www.kaggle.com/datasets/rabieelkharoua/cancer-prediction-dataset)
- [Diabetes Dataset](https://www.kaggle.com/datasets/mathchi/diabetes-data-set)

### 7. Run the Notebook Using VS Code
1. Install "Jupyter" extension
2. Open `notebook_medical_agent.ipynb`
3. Click "Select Kernel" → Choose your `venv` Python
4. Run cells sequentially from top to bottom!

## 💡 Usage Examples

### Database Queries:
```python
ask_medical_agent("How many patients have heart disease in the dataset?")
ask_medical_agent("What is the average age of cancer patients?")
ask_medical_agent("What is the average BMI of diabetic vs non-diabetic patients?")
```

### Web Search Queries:
```python
ask_medical_agent("What are the symptoms of diabetes?")
ask_medical_agent("What is coronary heart disease?")
ask_medical_agent("What are treatment options for cancer?")
```

## 📝 Requirements

- Python 3.13.2 was used
- See `requirements.txt` for all dependencies

## 👨‍💻 Author
GitHub: [@NahidMuntasir7](https://github.com/NahidMuntasir7)
