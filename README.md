# AiGateway - Gemini API Integration

This is an ASP.NET Core Web API project that acts as an intelligent gateway for communicating with the Google Gemini API. It is designed to provide smart content generation, specifically tailored for recipe creation based on available ingredients and interactive text-based survival games.

## Features
- **Google Gemini Integration:** Communicates with the `gemini-2.5-flash` model using custom-tailored system prompts.
- **Rate Limiting:** Built-in protection using a `FixedWindowLimiter` (5 requests per minute) to manage traffic and prevent abuse.
- **Structured Output:** Enforces JSON-only responses, making it easy to integrate with frontend applications.
- **Secure Configuration:** Uses environment variables (`.env` file) to manage API keys securely.

## Prerequisites
- **.NET 8.0 SDK** or later.
- **Google Gemini API Key** (Get it from [Google AI Studio](https://aistudio.google.com/)).

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/LEAH91R/MCP-PROJECT-.NET](https://github.com/LEAH91R/MCP-PROJECT-.NET)
   cd AiGateway
Configure Environment Variables:
Create a .env file in the project root directory and add your API key:

Plaintext
GEMINI_API_KEY=your_actual_api_key_here
Running the Project
To run the project, execute the following command in your terminal:

Bash
dotnet run
The API will be available at the address configured in your launchSettings.json (typically http://localhost:5202).

API Usage
Chat Endpoint
POST /api/Gemini/chat

Content-Type: application/json

Body: A string representing the user's prompt (e.g., a list of ingredients).

Technology Stack
Framework: ASP.NET Core Web API

Rate Limiting: Microsoft.AspNetCore.RateLimiting

Configuration: DotNetEnv

Communication: HttpClient
