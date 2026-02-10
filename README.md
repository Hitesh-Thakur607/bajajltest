🚀 Chitkara BFHL REST API

Production-ready REST API built with Node.js and Express for the BFHL assignment.
Implements structured responses, validation, security middleware, and external AI integration.

🔗 Live API
https://YOUR-RENDER-URL.onrender.com

✅ Features

Fibonacci series generation

Prime number filtering

LCM & HCF computation

AI-powered single-word responses (Google Gemini)

Health check endpoint

Robust validation & error handling

Rate limiting and security headers

🛠 Tech Stack

Node.js

Express.js

Google Gemini API

Helmet

Express Rate Limit

📌 API Endpoints
✅ Health Check
GET /health


Response

{
  "is_success": true,
  "official_email": "student@chitkara.edu.in"
}

✅ Main Endpoint
POST /bfhl


Send exactly one key per request.

Fibonacci
{
  "fibonacci": 7
}

Prime Numbers
{
  "prime": [2,4,7,9,11]
}

LCM
{
  "lcm": [12,18,24]
}

HCF
{
  "hcf": [24,36,60]
}

AI Response
{
  "AI": "What is the capital of Maharashtra?"
}


Output

{
  "is_success": true,
  "official_email": "student@chitkara.edu.in",
  "data": "Mumbai"
}

⚙️ Run Locally
1️⃣ Install dependencies
npm install

2️⃣ Create .env

Copy the example:

cp .env.example .env


Add:

CHITKARA_EMAIL=student@chitkara.edu.in
PORT=8080
GEMINI_API_KEY=YOUR_API_KEY

3️⃣ Start Server
npm start


Server runs at:

http://localhost:8080

🧪 Testing

Use Postman 

🔐 Environment Variables
Variable	Description
CHITKARA_EMAIL	Official email for responses
PORT	Server port
GEMINI_API_KEY	Google Gemini API key

⚠️ Never commit .env.

🚀 Deployment

Hosted on Render with public accessibility as required.

✅ Response Format

All successful responses:

{
  "is_success": true,
  "official_email": "YOUR_EMAIL",
  "data": ...
}


Errors return appropriate HTTP status codes with:

{
  "is_success": false,
  "error": "message"
}

👨‍💻 Author

Hitesh Thakur
Chitkara University — Class of 2027
