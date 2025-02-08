# genai-in-action-on-databricks
 Resources and content for the 'GenAI in Action on Databricks' presentation, delivered at the Spark+AI Meetup held at the Databricks Bellevue Office on November 13, 2024.

## Architecture - Overview
![Architecture_Overview](images/arch_overview.png)

## Architecture - Detailed
![Architecture_Overview](images/arch_detailed.png)

## Project Overview
This demo is designed to process and analyze product reviews for a global camera company. It integrates multiple AI models to handle tasks such as transcription, translation, sentiment analysis, and content generation. Here's an overview of its workflow:
1. **Audio Transcription**: `OpenAI's Whisper` transcribes audio-based reviews into text for further processing.
2. **Text Reviews Ingestion**: Textual reviews are ingested directly into the system.
3. **Text Translation**: `Meta's Llama 3.3` translates multilingual reviews into English language to ensure consistency in analysis.
4. **Sentiment Analysis**: `Llama 3.3` performs sentiment analysis to classify customer feedback as positive, neutral, or negative.
5. **Issue Classification**: Negative reviews are further categorized using `Llama 3.3` to identify specific issues with products.
6. **Report Generation**: Insights from sentiment and issue classification are compiled into detailed reports using `Llama 3.3`.
7. **Instagram Content Generation**: Marketing content based on positive reviews is created using `Llama 3.3` and `Databricks+Shutterstock's ImageAI` for social media campaigns.
8. **Report Translation**: Final reports are translated into multiple languages using `Llama 3.3` for global distribution.
This architecture leverages advanced AI tools like `OpenAI Whisper`, `GTE Large`, and `Meta's Llama 3.3 to streamline multilingual review processing and provide actionable insights for marketing and product improvement strategies.

Note: Llama 3.1 has been replaced by the latest Llama 3.3.

For more details, view the PDF: [Demo PDF](GenAI_in_Action_on_Databricks_-_Harshit_Rai.pdf)

## Steps to Execute the Code:

1. Update the `variables` in the `databricks.yml` file to use the desired models. These details can be obtained from the `Serving` section in Databricks UI. 
2. Also, update the `dev` and `prod` workspace host as well as the `serving_endpoint_url` variable in `databricks.yml` file.
3. Depending on whether you're using Databricks on Azure or AWS, comment/uncomment the code in the `resources/Spark+AI_GenAI_Demo.yml` file. Specific details are provided in the file.
4. Once this is done, follow the instructions in the README.md file inside the `genai_in_action_on_databricks` to deploy and run the Databricks Asset Bundle.

Known Issue:
If you're using Azure on Databricks and you see the following error, you might need to increase your quota.
![Azure_Error](images/azure_error.png)

