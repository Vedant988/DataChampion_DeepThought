# Company Intelligence Extractor using Gemini + Wikipedia + Web Scraping

## 🔍 Overview
An automated business intelligence pipeline that extracts, validates, and analyzes company data using web scraping, Wikipedia, and Google's Gemini LLM. The system processes company websites to produce structured metadata and industry-specific insights.

## ✨ Key Features
- **Web Scraping**: Extracts clean textual content from company websites using BeautifulSoup and requests
- **Wikipedia Integration**: Intelligently identifies and validates official Wikipedia pages through semantic search
- **Metadata Extraction**: Retrieves structured company information (CEO, Founders, Revenue, etc.) via "Gemini Pro" Large Language Model
- **Industry Classification**: Categorizes companies as F&B, Manufacturer, Brand, or Distributor
- **Domain Relevance**: Analyzes relevance to specific sectors (nutraceuticals, probiotics, fortification)

## 🛠️ Technologies
- **Web Scraping**: BeautifulSoup4, Requests
- **LLM Integration**: LangChain, Google Gemini Pro
- **Data Processing**: Pandas

## 📊 Sample Output: Nestle

### Input
```
Company Name: Nestle
Website: www.nestle.com
```

### Output
```json
{
  "CEO": "Mark Schneider",
  "Founder": "Henri Nestlé",
  "Founded": "1866",
  "Industry": "Food and Beverage",
  "Products": "Baby food, Coffee, Dairy products, Breakfast cereals, Confectionery, Bottled water, Ice cream",
  "Headquarters": "Vevey, Switzerland",
  "Revenue": "CHF 92.6 billion (2023)",
  "Employees": "273,000",
  "Summary": "Nestlé S.A. is a Swiss multinational food and beverage processing conglomerate headquartered in Vevey, Switzerland. It is the largest food company in the world, measured by revenue and other metrics. Nestlé produces various products including baby food, medical food, bottled water, breakfast cereals, coffee, confectionery, dairy products, ice cream, and pet foods.",
  "company_type": "F&B",
  "is_relevant": true,
  "is_fortification_potential": true,
  "notes": "Nestlé is highly relevant due to its significant presence in nutrition, health science, and fortified food products. The company has an extensive history of food fortification across multiple product lines, especially in developing markets."
}
```

## 🚀 Use Cases
- Market research and competitive analysis
- Investment due diligence
- Lead generation for specific industries
- Automated company profiling
- Domain-specific filtering (F&B, nutraceuticals, probiotics)

## 📋 Setup and Usage
1. Clone the repository
   ```bash
   git clone https://github.com/Vedant988/DataChampion_DeepThought.git
   cd DataChampion_DeepThought
   ```
   
2. Install the required dependencies
   ```bash
   pip install -r requirements.txt
   ```
   
3. Set your Google API key in the environment
   ```bash
   export GOOGLE_API_KEY="your-api-key"
   ```
   
4. Prepare your input CSV file with company data
   ```csv
   x,Company Name,Website
   1,Nestle,www.nestle.com
   2,Dr. Reddy's Laboratories,www.drreddys.com
   3,Coca,colacompany.com
   4,Pfizer,www.pfizer.com
   5,PepsiCo,www.pepsico.com
   ```
   
5. Run the extraction script
   ```bash
   python company_intelligence.py
   ```

## 📊 Pipeline Steps
The extraction process follows these steps:

1. **Website Content Extraction**:
   - Validates and formats URLs
   - Extracts text from paragraph tags
   - Applies error handling for failed requests

2. **Wikipedia Information Retrieval**:
   - Searches for official Wikipedia pages
   - Validates results via title matching and content analysis
   - Retrieves structured company information

3. **Gemini LLM Analysis**:
   - Processes website content using Google's Gemini Pro
   - Determines company type, industry relevance, and fortification potential
   - Generates structured insights in JSON format

4. **Results Aggregation**:
   - Combines information from all sources
   - Produces unified company intelligence records
   - Handles errors and provides fallback data when sources fail

## ⚠️ Requirements
- Python 3.8+
- Google API key for Gemini Pro access
- Input CSV with company names and website URLs
- Required packages: pandas, requests, beautifulsoup4, langchain, python-dotenv

## 📝 License
[MIT License](LICENSE)
