# OPEN RESEARCHER

This project is a research helper that uses several AI tools and web crawling to collect information on any topic. It creates search queries, visits web pages, checks if the content is useful, and produces a detailed report.

## File Versions

There are two versions of this tool:

- **open-researcher-openai.py**: Uses the OpenAI API.
- **open-researcher-llama.py**: Uses Llama and Groq for free access. Choose this if you do not have an OpenAI API key.

## Features

- Automatic creation of search queries using AI
- Simultaneous web page crawling and content pulling
- Evaluation of content usefulness
- Repeated improvement of research based on findings
- Complete report creation
- using crawl4AI which uses a headless browser to scrape the web so we get no rate limits

## Setup

## Clone the repository
``` bash
https://github.com/sandeep-chakraborty/Open-researcher.git
```

### 1. API Keys Needed

You need to get the following keys:

1. **OpenAI API Key** (Optional – for the alternative AI option)
   - Go to: [https://platform.openai.com/api-keys](https://platform.openai.com/api-keys)
   - Sign up or log in
   - Create a new API key
   - Place the key in the `OPENAI_API_KEY` field in your `.env` file

2. **SerpAPI Key**
   - Go to: [https://serpapi.com/](https://serpapi.com/)
   - Register an account
   - Find your API key in your dashboard
   - Place the key in the `SERPAPI_API_KEY` field in your `.env` file

3. **Groq API Key** (Optional – for the alternative AI option)
   - Visit: [https://console.groq.com/](https://console.groq.com/)
   - Sign up for an account
   - Generate your API key
   - Place the key in the `GROQ_API_KEY` field in your `.env` file

### 2. Environment File

Use the provided `.env.example` file as a guide.

### 3. Installing Dependencies

Clone the repository and create your `.env` file based on `.env.example`. Then run:

```bash
pip install -r requirements.txt
```
After running this run:
```bash
crawl4ai-setup
```

### 4. Running the Project

- Ensure all API keys are set correctly in your .env file.
- Update the `DEFAULT_MODEL` in the file to your desired model, i have used `gpt-4o-mini` and `llama-3.1-8b-instant`

Run the script:

```bash
python open-researcher.py
```
or
```bash
python open-researcher-openai.py
```

Enter your research query when prompted.

Specify the maximum number of search rounds (the default is 10).

# TODO
- Final result to MD
- Add a GUI
