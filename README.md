# Core Functionality

1. **Project Connection**:
   - User provides a W&B project name
   - Clippy connects to the project via wandb.API
   - Clippy greets with "What do you want to do today?"

2. **Data Retrieval**:
   - Fetch experiment configurations (hyperparameters, model architecture, etc.)
   - Retrieve summary metrics (accuracy, F1, loss, etc.)
   - Access code states/versions used in experiments
   - Get run timestamps and metadata

3. **Query Processing**:
   - Parse natural language questions about the project
   - Translate user intent into appropriate W&B API calls
   - Apply relevant filters and sorting to fetch precisely what's needed

4. **Analysis & Insights**:
   - Identify best-performing experiments by specified metrics
   - Detect performance trends across experiment iterations
   - Compare configurations between experiments
   - Explain performance differences between runs
   - Suggest specific configuration changes to improve target metrics

5. **Experiment Recommendations**:
   - Based on historical performance, recommend parameter adjustments
   - Estimate impact of suggested changes on key metrics
   - Provide rationale for recommendations

6. **Mock Experiment Launch**:
   - Simulate launching new experiments with suggested configurations
   - Track these "proposed experiments" in the conversation context

7. **Multi-turn Conversation**:
   - Maintain context across multiple user queries
   - Reference previous questions and answers
   - Allow follow-up questions about specific experiments

The system should handle various query types including:
- "What is the best experiment by [metric]?"
- "Why is my accuracy decreasing in recent runs?"
- "How can I improve the performance of my best model?"
- "Which experiment had the highest F1 score?"
- "What changed between experiment A and experiment B?"