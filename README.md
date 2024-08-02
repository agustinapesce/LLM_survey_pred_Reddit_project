Estimating Public Opinion with Large Language Models 

1. Motivation

Survey research plays a crucial role in informing policy decisions, yet challenges such as non-response rates and attrition have risen in the past decades. Large Language 
Models (LLMs) offer a promising cost-effective solution to provide in-silico answers that can serve as results screenings to assist survey polls. However, implementing LLMs for 
social sensing presents challenges, including biased behavior and limited context understanding.

In this study, we evaluate the quality of LLMs in predicting survey outcomes on public opinion matters using data from the American National 
Election Studies (ANES) 2020 survey. We also investigate how LLM performance is influenced by exposure to social media discussions on specific topics, using Reddit comments. 

Our analysis reveals mixed evidence regarding the accuracy of LLM predictions, with variations across different prompts and models. We find that while LLMs can provide reasonably 
accurate predictions for some policy issues, they may also exhibit biases and produce polarized outcomes, particularly when exposed to social media discussions. Although LLM’s social sensing capabilities could 
not show accurate results for all policies in this study, the positive effect of in-context learning provided by social media discussions for some of the topics encourages further 
developments in this research direction. 

3. Comments data (data_praw.ipynb)
   
Using PRAW on r/news to retrieve discussions on selected topics during 2020.

Topics: 
* Abortion
* Climate Change
* Gun Control
* Immigration
* Health Care

4. LLMs and prompting (gpt-3.5-turbo-0125_outputs.ipynb & mistral_SE.ipynb)
   
GPT-3.5. and Mistral implementation with self-extent for increased prompt length were used.
Prompting techniques for both included zero-shot prompt and zero-shot with Reddit comments at inference time.
   
6. Data cleaning (gpt-3.5-turbo-0125_outputs.ipynb & mistral_cleaning.ipynb)
   
Cases were answer didn't add up to a 100% were deleted for GPT-3.5.
Since Mistral output was more problematic a more sophisticated post-processing was performed. Some small deviations from the desired output were solved with Regex
methods and as cases were results added up to 100% were so few a normalization was implemented with the given output.
   
8. Analysis (graphs_stats_results.ipynb)
   
Bar graphs and boxplots were built to visualize the results. A table also communicates mean and standard deviation differences compared to the actual distribution of answers.

10. Repository
    
More information on the workflow and analyses can be found in the report "final_report.pdf"
