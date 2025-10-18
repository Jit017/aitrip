# 🌍 AI Trip - Intelligent Travel Planning Agent

An AI-powered travel planning application that uses LangGraph and multiple AI models to create comprehensive travel itineraries. The system combines weather information, place search, expense calculations, and currency conversion to provide personalized travel recommendations.

## ✨ Features

- **🤖 AI-Powered Planning**: Uses LangGraph with multiple AI models (Groq, OpenAI) for intelligent travel planning
- **🌤️ Weather Integration**: Real-time weather information for destinations
- **📍 Place Search**: Find and recommend places, restaurants, and attractions
- **💰 Expense Calculator**: Calculate trip costs and budget planning
- **💱 Currency Conversion**: Real-time currency conversion for international travel
- **🌐 Web Interface**: Beautiful Streamlit frontend with chat interface
- **⚡ FastAPI Backend**: RESTful API for scalable deployment
- **📊 Visual Workflow**: Mermaid graph visualization of the planning process

## 🏗️ Architecture

The application follows a modular architecture with the following components:

```
aitrip/
├── agent/                 # AI agent workflow using LangGraph
├── tools/                 # Specialized tools for travel planning
├── utils/                 # Utility functions and helpers
├── config/                # Configuration files
├── prompt_library/        # AI prompts and templates
├── notebook/              # Jupyter notebooks for experimentation
├── main.py               # FastAPI backend server
├── streamlit_app.py      # Streamlit frontend
└── requirements.txt      # Python dependencies
```

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- API keys for:
  - Groq API
  - OpenAI API (optional)
  - Google Places API
  - Weather API

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Jit017/aitrip.git
   cd aitrip
   ```

2. **Create virtual environment**
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys
   ```

5. **Run the application**

   **Backend (FastAPI)**
   ```bash
   python main.py
   # or
   uvicorn main:app --reload
   ```

   **Frontend (Streamlit)**
   ```bash
   streamlit run streamlit_app.py
   ```

## 🔧 Configuration

Create a `.env` file in the root directory with the following variables:

```env
# AI Model APIs
GROQ_API_KEY=your_groq_api_key
OPENAI_API_KEY=your_openai_api_key

# Google Services
GOOGLE_PLACES_API_KEY=your_google_places_api_key

# Weather API
WEATHER_API_KEY=your_weather_api_key

# Other configurations
MODEL_PROVIDER=groq  # or openai
```

## 🛠️ Available Tools

### Weather Information Tool
- Get current weather conditions
- Forecast information for destinations
- Weather-based travel recommendations

### Place Search Tool
- Find restaurants, hotels, attractions
- Get place details and reviews
- Location-based recommendations

### Expense Calculator Tool
- Calculate trip costs
- Budget planning and tracking
- Cost breakdown by category

### Currency Conversion Tool
- Real-time exchange rates
- Multi-currency support
- Travel budget conversion

## 📱 Usage

### Web Interface

1. Open your browser and go to `http://localhost:8501`
2. Enter your travel query in the chat interface
3. Example queries:
   - "Plan a 5-day trip to Goa"
   - "Find budget hotels in Paris for 3 nights"
   - "What's the weather like in Tokyo next week?"
   - "Convert $1000 to EUR for my Europe trip"

### API Endpoints

**POST /query**
```json
{
  "question": "Plan a trip to Bali for 7 days"
}
```

Response:
```json
{
  "answer": "Here's your comprehensive 7-day Bali itinerary..."
}
```

## 🧪 Development

### Running Tests
```bash
pytest tests/
```

### Code Formatting
```bash
black .
isort .
```

### Type Checking
```bash
mypy .
```

## 📊 Workflow Visualization

The application generates Mermaid graphs showing the AI workflow process. These are saved as `my_graph.png` in the project root.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [LangChain](https://github.com/langchain-ai/langchain) for the AI framework
- [LangGraph](https://github.com/langchain-ai/langgraph) for workflow management
- [Streamlit](https://streamlit.io/) for the web interface
- [FastAPI](https://fastapi.tiangolo.com/) for the backend API

## 📞 Support

If you encounter any issues or have questions, please:

1. Check the [Issues](https://github.com/Jit017/aitrip/issues) page
2. Create a new issue with detailed information
3. Contact the maintainers

---

**Happy Traveling! 🌍✈️**
