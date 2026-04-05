# n8n - Locally Extract from PDFs And write to excel (.xlsx)

n8n workflow designed to automate the extraction of structured data from PDF documents using a local Large Language Model (LLM) and saving the results into a formatted Excel spreadsheet. Works fully locally - no data is upload to any online service.

# Workflow

1.  **Read:** Reads all PDF files from local directory (on the host machine, using docker).
2.  **Extract:** Uses local LLM **Llama 3.2** to analyze document contents and extract:
    *   Name
    *   Age
    *   Known Programming Languages
    *   Additional Information/Notes
3.  **Write:** Appends the structured data into an `.xlsx` file on the host machine.

# Requirements

n8n 2.14.2
(optional) Docker Desktop 28.5.1, build e180ab8
llama 3.2
