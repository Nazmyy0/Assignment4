 README: Applied AI Weather Assistant

 Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/your-repo/weather-assistant.git && cd weather-assistant
   ```
2. Create a virtual environment (optional):
   ```bash
   python3 -m venv venv && source venv/bin/activate  
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up `.env` file:
   ```plaintext
   API_KEY=your_openai_api_key
   BASE_URL=your_openai_base_url
   LLM_MODEL=your_model_name
   WEATHER_API_KEY=your_weather_api_key
   ```
5. Run:
   ```bash
   python weather_assistant.py
   ```

 Implementation
Three AI agents:
- Basic: Provides direct weather responses.
- CoT: Thinks step-by-step before answering.
- ReAct: Uses iterative reasoning and actions.
 Examples
- Basic: “What’s the weather in Paris?” → “15°C, cloudy.”
- CoT: “Temp difference between Cairo (20°C) & London (10°C)?” → “10°C.”
- ReAct: “Compare New York & LA weather.” → “NY: 12°C, cloudy. LA: 25°C, sunny.”

 Analysis
- Basic: Fast but lacks deep reasoning.
- CoT: More accurate but slower.
- React: Best for complex queries but higher cost.

 Challenges & Fixes
- Handled API errors with better messaging.
- Improved complex query processing using CoT & ReAct.
- Cached results to optimize efficiency.

 Evaluation
Run and compare agent responses:
```bash
python weather_assistant.py
```
Choose 'Option 2' and rate responses (1-5). Results saved in `evaluation_results.csv`.

 Conclusion
ReAct delivers the best accuracy but at a higher cost. Future improvement: add memory for better context.

