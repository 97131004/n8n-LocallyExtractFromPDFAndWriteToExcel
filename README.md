# n8n: Locally extract data from PDFs and write to Excel

This n8n workflow (proof of concept) automates the extraction of structured data from PDF documents using a local Large Language Model (LLM) and an AI agent. It processes files and saves the results into a formatted Excel spreadsheet. The entire process runs fully locally - no data is ever processed by any online service.

# Workflow

![workflow](https://github.com/97131004/n8n-LocallyExtractFromPDFAndWriteToExcel/blob/c768b4e8bb384cbf9df3bdb9bf2a4874690e36ae/workflow.PNG)

1.  **Read:** Reads all PDF files from local directory (on the host machine, using docker).
2.  **Extract:** Uses local LLM **Llama 3.2** to analyze document contents and extract:
    *   Name
    *   Age
    *   Known Programming Languages
    *   Additional Information/Notes
3.  **Write:** Appends the structured data into an `.xlsx` file on the host machine.

# Requirements

* Self-hosted n8n 2.14.2 (with Docker Desktop 28.5.1, build e180ab8) 
* llama 3.2 LLM (installed via docker)
* Shared/mounted folder between the host machine and the Docker container at `/home/node/docker_share`

# Test case

`1.pdf`<br><br>
![workflow](https://github.com/97131004/n8n-LocallyExtractFromPDFAndWriteToExcel/blob/152c728ce7000d2c1d0f839ebfee20afca24a123/TestFiles/test1.PNG)
<br>
<br>
`2.pdf`<br><br>
![workflow](https://github.com/97131004/n8n-LocallyExtractFromPDFAndWriteToExcel/blob/152c728ce7000d2c1d0f839ebfee20afca24a123/TestFiles/test2.PNG)
<br>
<br>
`results.xlsx`<br><br>
![workflow](https://github.com/97131004/n8n-LocallyExtractFromPDFAndWriteToExcel/blob/c8d894458f45cd7ed1a58ec9504eed8eabb36d0e/Results/results.PNG)

# License
MIT
