prompt for making backend:
```text
Build an agent backend using google agent development kit following the documentation.
https://google.github.io/adk-docs/

It's session is in memory for each user. The agent/agent team is supposed to help in data visualization and data insights when uploaded dataset in mongodb.

It should be async i think because it needs to support multiple users. Use the InMemoryMemoryService, And for data insights and interesting points please maintain them in state of conversations using the the appropriate state as per docs.

Use the InMemorySessionService as well. i think you need to create new temp and discardable session ids and close the sessions when user is done as the backend use is for a visit and go away website where user can just visit website, use the application and leave without any login, etc...

Make sure it is deployable on free things like railway or render backend in python. There is an option to use the thing as api_server via adk and fastapi as per the docs so please check that out as well.

That's all for the technical stuff.
Here's my idea:
Your Innovation Stack:
Google ADK + MongoDB = Perfect Combo
python# Your Custom Agent using Google ADK
from google_agent_sdk import Agent
import pymongo

class DataCuriosityAgent(Agent):
    def __init__(self):
        # MongoDB connection
        self.mongo_client = MongoClient()
        self.db = self.mongo_client['curiosity_data']
        
        # Google ADK for AI capabilities
        super().__init__(
            name="CuriosityExplorer",
            instructions="Be curious about data anomalies"
        )
    
    def analyze_with_curiosity(self, query):
        # Step 1: MongoDB query
        data = self.fetch_relevant_data(query)
        
        # Step 2: Your custom curiosity logic
        insights = self.find_patterns(data)
        curiosities = self.generate_curiosities(insights)
        
        # Step 3: Google ADK for smart responses
        response = self.generate_response(insights, curiosities)
        
        return response
🎯 Your Unique Value Proposition:
What You're Building:
"First AI Agent that makes MongoDB data exploration conversational and curious"
Innovation Points:

MongoDB + Conversational AI - No one has done this properly
AI-generated follow-up questions - Based on MongoDB query results
Vector search + Curiosity - Find similar patterns across datasets
Persistent conversation memory - Store in MongoDB, reference via ADK

🏗️ Architecture with Both Platforms:
MongoDB Track Compliance:
javascript// MongoDB Features You'll Showcase:
{
  // 1. Vector Search for dataset discovery
  dataset_embeddings: [...],
  
  // 2. Aggregation for insights
  analysis_pipeline: [...],
  
  // 3. Document flexibility
  conversation_history: {
    user_questions: [...],
    ai_curiosities: [...],
    discovered_patterns: [...]
  }
}
Google ADK Track Compliance:
python# Google Agent Features:
class CuriosityAgent:
    def generate_curiosities(self, mongodb_results):
        # Use Google AI to analyze MongoDB data
        # Generate intelligent follow-up questions
        # Maintain conversation context
        pass
🚀 Dual Hackathon Strategy:
For MongoDB Judges:
"Look! We're using MongoDB's vector search to find related datasets, aggregation pipelines for complex analysis, and flexible documents to store conversation history!"
For Google ADK Judges:
"Look! Our agent intelligently analyzes data patterns and generates curious follow-up questions, maintaining context across conversations!"
💡 Implementation Approach:
Your Custom Curiosity Engine:
pythonclass MongoCuriosityEngine:
    def __init__(self):
        # MongoDB for data storage & retrieval
        self.mongo = MongoClient()
        
        # Google ADK for AI reasoning
        self.agent = CuriosityAgent()
    
    def explore_data(self, user_query):
        # 1. MongoDB: Find relevant datasets
        datasets = self.mongo.vector_search(user_query)
        
        # 2. MongoDB: Run analysis aggregations  
        insights = self.mongo.aggregate_analysis(datasets)
        
        # 3. Your Logic: Detect curiosity triggers
        curiosities = self.detect_anomalies(insights)
        
        # 4. Google ADK: Generate smart questions
        questions = self.agent.generate_questions(curiosities)
        
        # 5. MongoDB: Store conversation
        self.mongo.save_conversation(user_query, insights, questions)
        
        return {
            'insights': insights,
            'curious_questions': questions,
            'suggested_exploration': self.agent.suggest_next_steps()
        }
🎪 Demo Selling Points:
"We built the first AI that gets curious about your data!"
Live Demo:

User asks question → MongoDB finds data
AI analyzes → Finds interesting pattern
AI says: "Wait, I found something weird..."
Shows follow-up suggestions
User clicks → Deeper exploration continues

Technical Wow Factors:

✅ MongoDB vector search for smart dataset matching
✅ Custom aggregation pipelines for insights
✅ Google ADK for conversational AI
✅ Your innovation: Curiosity-driven exploration

🏆 Why This Wins Both Tracks:
MongoDB: "Best use of our advanced search and aggregation features"
Google ADK: "Most innovative conversational agent for data exploration"
Ready to build the future of curious data exploration?
```