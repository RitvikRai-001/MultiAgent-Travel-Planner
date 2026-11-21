Multi-Agent Travel Planner
This is a Multi-Agents travel planner that turns a natural-language trip request into a practical travel plan with flight suggestions, hotel ideas, and a day-by-day itinerary.

The project uses a multi-agent workflow built with LangGraph.
Why this project?
Planning a trip usually means jumping between multiple websites, tools, and spreadsheets. This project brings that flow into one experience by combining:
- A flight-search agent,
- A hotel-research agent,
- An itinerary-planning agent, and
- A final-response agent,
all coordinated through a LangGraph workflow.
Diagram (visible portion)
1. Flight Agent – Searches for flights and selects the best options.
2. Hotel Agent – Searches hotels and compares options.
3. Itinerary Agent – Creates a day-wise travel itinerary based on the trip.
4. Final Response Agent – Combines all information and generates the final response.

FLIGHT AGENT
Searches flights and finds best options

Tools / APIs
Free Flight API (AviationStack)
Tavily Search

HOTEL AGENT
Searches hotels and compares options

Tools / APIs
Tavily Search
Google Places API (Optional)

ITINERARY AGENT
Creates day-wise itinerary, places to visit, activities

Tools / APIs
Tavily Search
Google Maps API (Places, Directions)

FINAL RESPONSE AGENT
Combines all information and generates final response

Tools / APIs
Groq LLM (Llama 3)
Tavily Search

SHARED STATE (TravelState)
user_query | flight_results | hotel_results | itinerary | final_response | messages | ...

PostgreSQL
Long-Term Memory
(Stores conversations & state)
✓ Conversation history
✓ User preferences
✓ Agent outputs & state updates

Flow of Execution
Agent Output -> Stat[e]
State Persisted
Agents