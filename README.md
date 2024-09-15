# HackTheNorth-Financial-report (Company Reports summarizer)

This project converts company reports, such as annual financial statements, into a structured and understandable JSON format for easy analysis and viewing. It processes PDFs by dividing them into segments, sends these segments to OpenAI’s GPT-3.5 API for summarization, and outputs the results in a JSON file.

## Features

- **Segmented PDF Processing**: The tool reads PDF reports and processes them in manageable segments (48 pages by default) to avoid token limits of the GPT-3.5 model.
- **AI-Powered Summarization**: OpenAI’s GPT-3.5 API is used to generate detailed summaries for each PDF segment.
- **Comprehensive Summary**: Once all segments are processed, the tool generates a comprehensive summary based on all segments combined.
- **JSON Output**: The final summary is stored in a JSON file, making it easy to analyze or integrate into other systems.

## Example Output

Here’s an example JSON output for the IBM 2023 Annual Report:

```json
{
  "IBM_2023_Annual_Report": {
    "overview": {
      "title": "2023 Annual Report",
      "chairman_and_ceo": "Arvind Krishna",
      "salutation": "Dear IBM Investor:",
      "message": "In 2023, we made significant progress in our journey to become a more innovative and focused company, built around the two most transformational technologies of our time: hybrid cloud and AI.",
      "content": [
        "We executed against a proven strategy, refined our portfolio, expanded our ecosystem of partners, and enhanced productivity throughout IBM.",
        "We also continued to address the evolving needs of our clients. As AI becomes a top priority, our clients are using watsonx – IBM's flagship AI and data platform – to help revolutionize customer service, modernize countless lines of code, and automate enterprise tasks to boost employee productivity.",
        "I have never been more confident in IBM’s direction. Today’s IBM is more capable and more productive. We have a strong portfolio and a solid foundation to support sustainable growth. And we are delivering on our promise to be the catalyst that makes the world work better.",
        "For the year, IBM generated $61.9 billion in revenue, up 3% at constant currency, and $11.2 billion of free cash flow, up $1.9 billion year-over-year."
      ],
      "performance_summary": {
        "key_metrics": {
          "total_revenue": "$61.9 billion",
          "revenue_growth": "3%",
          "free_cash_flow": "$11.2 billion",
          "year_over_year_free_cash_flow_increase": "$1.9 billion"
        },
        "business_segments": {
          "Software": {
            "revenue": "$26,308 million",
            "percentage_of_total": "42.5%",
            "year_over_year_change": "5.1%"
          },
          "Consulting": {
            "revenue": "$19,985 million",
            "percentage_of_total": "32.2%",
            "year_over_year_change": "4.6%"
          },
          "Infrastructure": {
            "revenue": "$14,593 million",
            "percentage_of_total": "23.6%",
            "year_over_year_change": "-4.5%"
          },
          "Financing": {
            "revenue": "$741 million",
            "percentage_of_total": "1.1%",
            "year_over_year_change": "14.8%"
          }
        }
      }
    },
    "financial_performance": {
      "year_in_review": [
        {
          "segment": "Software",
          "details": {
            "total_revenue": "$26,308 million",
            "hybrid_platform_solutions": "$18,693 million",
            "transaction_processing": "$7,615 million",
            "gross_profit_margin": "80.1%",
            "pre_tax_income": "$6,571 million",
            "pre_tax_margin": "25.0%"
          }
        },
        {
          "segment": "Consulting",
          "details": {
            "total_revenue": "$19,985 million",
            "business_transformation": "$9,179 million",
            "technology_consulting": "$3,849 million",
            "application_operations": "$6,958 million",
            "gross_profit_margin": "26.6%",
            "pre_tax_income": "$1,918 million",
            "pre_tax_margin": "9.6%"
          }
        },
        {
          "segment": "Infrastructure",
          "details": {
            "total_revenue": "$14,593 million",
            "hybrid_infrastructure": "$9,215 million",
            "infrastructure_support": "$5,377 million",
            "gross_profit_margin": "56.0%",
            "pre_tax_income": "$2,421 million",
            "pre_tax_margin": "16.6%"
          }
        },
        {
          "segment": "Financing",
          "details": {
            "total_revenue": "$741 million",
            "client_financing": "$728 million",
            "gross_profit_margin": "48.1%",
            "pre_tax_income": "$374 million",
            "pre_tax_margin": "50.5%"
          }
        }
      ]
    }
  }
}
```

## Installation

To use the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Neufal777/HackTheNorth-Financial-report.git
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set your OpenAI API Key and environment variables:
   ```bash
   export OPENAI_API_KEY="your-api-key"
   export OPENAI_API_TYPE="api-type"
   export OPENAI_API_BASE="api-base"
   export OPENAI_API_VERSION="api-version"
   ```

4. Run the project with an example PDF file:
   ```bash
   python main.py (remember to change the pdf path in the main file)
   ```

## Usage

The tool reads the specified PDF file, processes it, and outputs the analysis in a JSON file. Modify the path to your PDF file in the script to analyze different documents.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or improvements, feel free to open an issue or submit a pull request.


---

This project was built for a hackathon with the goal of simplifying the analysis of company reports through AI.
