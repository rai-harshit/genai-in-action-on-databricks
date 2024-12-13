# genai-in-action-on-databricks
 Resources and content for the 'GenAI in Action on Databricks' presentation, delivered at the Spark+AI Meetup held at the Databricks Bellevue Office on November 13, 2024.

Steps to Execute the Code:
1. Create an ML compute cluster in Databricks on which you will run the code. Cluster details can be found in the `resources/cluster_spec.json` file.
2. Copy the cluster ID from the 'Compute' page in your Databricks workspace and update it in the `resources/Spark_AI_GenAI_Demo.yml` file.
3. Update the `databricks.yml` file with your dev workspace host.
4. In each of the notebooks, check for the code that queries the Databricks Serving Endpoint and update it with your workspace's serving endpoint link.
5. For Audio Transcription, you will have to sign up on `HuggingFace` and generate an API token to download the model.
6. Before running the `06_Report_Generation` and `07_Marketing_Content_Generation` notebooks, ensure that you have two volumes created inside the products schema: `reports` and `social_media`.
7. Once this is done, follow the instructions in the README.md file inside the `genai_in_action_on_databricks` to deploy and run the Databricks Asset Bundle. 
