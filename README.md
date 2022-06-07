# Thesis
This repository contains all the data files and code files that were used to derive the results of my master thesis. The following items were used in the analysis:

R MARKDOWN FILES CONTAINING CODE (.RMD)
**1. Data_Processing_Regulations.RMD**: This R Markdown contains the steps to transform the raw text data from the Raw_Data_Text folder into cleaned, tokenized data, so that it is ready for text analysis in Data_Analysis_H1_H2.RMD and Data_Analysis_H3_H4.RMD.
**2. Data_Processing_Metrics.RMD**: This R Markdown contains the steps to transform the raw text data from the ESG_Metrics_Text folder into with cleaned and tokenized data, so that it is ready for text analysis in Data_Analysis_H3_H4.RMD.
**3. Data_Analysis_H1_H2.RMD**: In the documents Data_Processing_Regulations.Rmd and Data_Processing_Metrics.Rmd, the data was cleaned and processed. In this markdown, analysis is performed on this processed data for Hypothesis 1 and Hypothesis 2 (quantity, readability and linguistic characteristics).
**4. Data_Analysis_H3_H4.RMD**: In the documents Data_Processing_Regulations.Rmd and Data_Processing_Metrics.Rmd, the data was cleaned and processed. In this markdown, analysis is performed on this processed data for Hypothesis 3 (Document similarity) and Hypothesis 4 (Keyword analysis).
**5. Data_Analysis_Robustness.RMD**: In the documents Data_Processing_Regulations.Rmd and Data_Processing_Metrics.Rmd, the data was cleaned and processed. In this markdown, robustness analysis is performed on this processed data for Hypothesis 3 (Document similarity) and Hypothesis 4, by using a variation (filtering on POS) on Processed_Data as input. 

RAW TEXT DATA (.txt)
**1. Raw_Data_Text**: This is a folder, containing raw txt. files. Every text file represents an ESG reporting standard. The file names correspond with their respective DOC_ID (see Meta_Data_Regulations.csv)
**2. ESG_Metrics_Text**: This is a folder, containing raw txt. files. Every text file represents an ESG key metric. The file names correspond with their respective Metric_ID (see Meta_Data_Metrics.csv)

RAW META DATA (.csv)
**1. Meta_Data_Regulations.csv**: This file contains the meta data on the regulations. 
**2. Meta_Data_Metrics.csv**: This file contains the meta data on the metrics. 

RAW DATA USED FOR FILTERING (.txt & .csv)
**1. stopwords.txt**: This text file contains a selection of stopwords, that were used to filter the text data in Data_Processing_Regulations.RMD and Data_Processing_Metrics.RMD. 
**2. Metrics_Keywords.csv**: This csv file contains the ESG key words that are used for H4 (Data_Analysis_H3_H4.RMD). 

PROCESSED DATA, RESULTING FROM APPLYING PROCESSING STEPS TO RAW DATA (.RData)
**1. Descriptive_Data.RData**: This data file contains the meta data for each regulation document and descriptive statistics, like the amount of words and the readability of the regulation document. Each row is uniquely identief by DOC_ID. 
**2. Processed_Data.RData**: This data file contains all the regulations data, split into tokens. This file can be obtained by running the Data_Processing_Regulations.RMD.
**3. Metrics_Data.RData**: This data file contains the text describing ESG metrics. This data is in a tokenized data format. The metrics data is used to benchmark the content of the regulations documents (measuring how many ESG topics are covered by the regulations).  



