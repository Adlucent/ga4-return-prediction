# A Return Prediction Model for Retailers Using GA4 Data

With return rates rising since 2020, it is increasingly important for retailers to understand the true value of a purchase. This repo contains a full solution for predicting, at the time of purchase, how much revenue from an order will be returned. It contains a series of Google Colab notebooks and is written primarily in Python, using this [BigQuery sample dataset](https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset) from Google Analytics 4.<br>
<br>
In these notebooks, you'll:
* Analyze, preprocess, and engineer a GA4 dataset from BigQuery and prepare it for modeling,
* Build, tune and evaluate three regression models that return order-level predictions for returned revenue, and
* Save the results into a table for visualization and further analysis.<br>
<br>

Notebooks Included:<br>
  1. Setup_&_EDA<br>
  2. Data_Cleaning_&_Encoding<br>
  3. Order_Level_Agg_and_Feature_Engineering<br>
  4. Customer_Level_Aggregation<br>
  5. Multicollinearity_Check_and_Joining_Data<br>
  6. Scale_Data_and_Customer_Segmentation<br>
  7. Model_Building_and_Evaluation<br>
<br>

Prerequisites and Initial Setup Requirements:<br>
* A Google Cloud Platform account and project<br>
* A GA4 BigQuery Export of the data you want to use in training the model<br>
* Return data at the order level that includes returned revenue, quantity returned, item returned, order ID and return date (If you don't have returns data already populating in GA4, you can merge it in from a separate file)<br>
<br>

Other GCP Tools Available:<br>
* **Vertex AI Workbench:** The Vertex AI Workbench within the GCP console has an integration with JupyterLabs where you can create managed or user-managed notebooks directly within GCP. If you’re handling sensitive data or need more scalable computing resources to process larger amounts of data, you can create a user-managed notebook within the workbench that runs on a Compute Engine virtual machine and open the .ipynb notebooks within that. Jupyter Labs within the Vertex AI workbench has all of the same features (and then some) as the version you typically have installed locally
* **AutoML**: Once you get to the model building step, AutoML could be a great alternative if your BigQueryML models are not performing as well as you’d like, if your training dataset is very large, or if you’re looking to fully automate and deploy your model for real-time or batch predictions. You can train AutoML models from within the Vertex AI Training section of the GCP console, or directly from your notebook using Python.<br>
<br>

For processing large data sets, you can also **connect Colab to a local runtime or upgrade to a hosted runtime**, or use JupyterLabs from the Vertex AI Workbench in the GCP console.<br>
