# Company Intelligence Extractor using Gemini + Wikipedia + Web Scraping

This project automates the process of extracting structured business intelligence for organizations using a hybrid pipeline combining:

Web scraping (BeautifulSoup + requests)

Wikipedia API search and content validation

Gemini Pro LLM (via LangChain)

Natural Language Understanding of unstructured HTML content

It fetches static data from official websites, retrieves structured information from Wikipedia, and then synthesizes detailed company metadata using Google's Gemini LLM. Ideal for market research, competitor profiling, investment analysis, and domain-specific filtering (e.g., nutraceuticals, probiotics, F&B sector).


📌 Features
✅ Scrape and clean static content (<p> tags) from a list of company websites
✅ Identify and validate official Wikipedia pages via semantic search and title-content validation
✅ Summarize organization metadata (CEO, Founders, Revenue, Industry, etc.) via Gemini LLM
✅ Analyze company category (F&B, Manufacturer, Brand, Distributor) and domain relevance
✅ Identify potential in Food Fortification industry using Gemini-powered NLU
✅ Clean error handling and fallback mechanisms (timeouts, invalid JSON, empty text)


📊 Sample Output
json
'''
Edit
{
  "CEO": "Albert Bourla",
  "Founder": "Charles Pfizer",
  "Founded": "1849",
  "Industry": "Pharmaceuticals",
  "Products": ["Vaccines", "Prescription Drugs"],
  "Headquarters": "New York City, USA",
  "Revenue": "$81.3B (2023)",
  "Employees": "79,000",
  "Summary": "Pfizer is an American multinational pharmaceutical corporation..."
}
'''
