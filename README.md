# Neural Information Retrieval System

| Name | Student Number | Tasks |
| --- | --- | --- |
| Kaishuo Wang | 300068284 | method1, method3 |
| Ralph Huo | 300069921 | result analysis |

### Inportant note
For this assignment, we have tried two methods. Therefore, we have included results and code for both of them.

### Detailed note about the functionality
In this folder, we have two files method1.ipynb and method3.ipynb. 

For method 1, we used the first method professor have provided in the assignment instruction which is use the result from assignment1 and re-calculate the cosine similarity using BERT word embadding and re-rank them according to the new cosine similarities.

For method 3, we use the third method professor have provided in the assignment instruction which is use the BERT word embadding from the begining to calculate the cosine similarity between query and documents. For this method, in order to save time, we have selected set of *relative* documents which contains at least one word of the query. However, this method is still taking over 20 minutes.

### How to run method1.ipynb and method3.ipynb
You need to run both files using Google Colab. First upload both files into you Google Drive, then search for Colaboratory using the *plus* sign at right bar. After that install Colaboratory plugin. Then double click the file in your Google Drive to open them using Colab. After you have opened the .ipynb file. You need to upload *topics_MB1-49.txt* and *Trec_microblog11.txt* for both method1 and method 3, and *Results_fromA1.txt* for method1 using the file icon at the left bar. I have include two images for what you Colab should looks like after you have done all previous steps.

After all previous steps, you can start to run the code. You need to go to the *runtime* manu at top, then click *run all*. It will run all cells. Or you can click the *run cell* button at left of each cell to run a single button. But if you are going to run each cell one by one, you will need to run them in order from top to bottom.

More detailed explainations will be included in the code.

### Algorithms, data structures, and optimization
For both mathods, we used BERT. We used a pretrained model for BERT and util.cos_sim for computing socine similarity from Huggingface. 

As for data structure, we used dataframe from pandas so store all the data in bothe methods.

For optimization, as I just mentioned, we limited the number of documents for each query in method 3 in order to same time.

#### First ten results for query 3 and 20 of method 1
MB003 Q0 32204788955357184 1 0.772 myRun  
MB003 Q0 32488312107175936 2 0.762 myRun  
MB003 Q0 29296574815272960 3 0.743 myRun  
MB003 Q0 29613127372898304 4 0.74 myRun  
MB003 Q0 32469924240695297 5 0.726 myRun  
MB003 Q0 29278582916251649 6 0.722 myRun  
MB003 Q0 33711164877701120 7 0.713 myRun  
MB003 Q0 32878302150529024 8 0.711 myRun  
MB003 Q0 31861291236724738 9 0.706 myRun  
MB003 Q0 32910196598636545 10 0.699 myRun  

MB020 Q0 32865855435968512 1 0.778 myRun  
MB020 Q0 32218912527482880 2 0.778 myRun  
MB020 Q0 31101259872215040 3 0.763 myRun  
MB020 Q0 29853985930219520 4 0.761 myRun  
MB020 Q0 30962906484969472 5 0.754 myRun  
MB020 Q0 29934471260151808 6 0.753 myRun  
MB020 Q0 29906116062220290 7 0.75 myRun  
MB020 Q0 31085134354583552 8 0.744 myRun  
MB020 Q0 33114843795951616 9 0.728 myRun  
MB020 Q0 33356942797701120 10 0.728 myRun  

#### First ten results for query 3 and 20 of method 3
MB003 Q0 32204788955357184 1 0.772 myRun  
MB003 Q0 32488312107175936 2 0.762 myRun  
MB003 Q0 29296574815272960 3 0.743 myRun  
MB003 Q0 29613127372898304 4 0.74 myRun  
MB003 Q0 32469924240695297 5 0.726 myRun  
MB003 Q0 29278582916251649 6 0.722 myRun  
MB003 Q0 33711164877701120 7 0.713 myRun  
MB003 Q0 32878302150529024 8 0.711 myRun  
MB003 Q0 31861291236724738 9 0.706 myRun  
MB003 Q0 32910196598636545 10 0.699 myRun  

MB020 Q0 32865855435968512 1 0.778 myRun  
MB020 Q0 32218912527482880 2 0.778 myRun  
MB020 Q0 31101259872215040 3 0.763 myRun  
MB020 Q0 29853985930219520 4 0.761 myRun  
MB020 Q0 30962906484969472 5 0.754 myRun  
MB020 Q0 29934471260151808 6 0.753 myRun  
MB020 Q0 29906116062220290 7 0.75 myRun  
MB020 Q0 31085134354583552 8 0.744 myRun  
MB020 Q0 33114843795951616 9 0.728 myRun  
MB020 Q0 33356942797701120 10 0.728 myRun  

### Discuss whether Method1 and Method3 were achieved better results than Assignment1:
Based on the result which we were tested from Method1 and Method3. We get a higher value than the result from Assignment1. Whatever for Interpolated Recall's value and Precision of the x first documents value are all higher than the result from Assignment1. Which indicated that we achieved better results than Assignment1.

### Evaluation
The best score for the result is 
Map:0.2456 (Using Method 3)
P@10:0.3327 (Using Method 1)
Based on the above data. We discovered that all the method has their strength and weakness. None of the methods all perfect. Therefore, we still need to improve our work to make it to be perfect.

### Results
#### Method 1
runid                  all myRun  
num_q                  all 49  
num_ret                all 49000  
num_rel                all 2640  
num_rel_ret            all 1957  
map                    all 0.2425  
gm_map                 all 0.1087  
Rprec                  all 0.2787  
bpref                  all 0.2365  
recip_rank             all 0.5775  
iprec_at_recall_0.00   all 0.6334  
iprec_at_recall_0.10   all 0.4690  
iprec_at_recall_0.20   all 0.3878  
iprec_at_recall_0.30   all 0.3239  
iprec_at_recall_0.40   all 0.2923  
iprec_at_recall_0.50   all 0.2525  
iprec_at_recall_0.60   all 0.1987  
iprec_at_recall_0.70   all 0.1587  
iprec_at_recall_0.80   all 0.1166  
iprec_at_recall_0.90   all 0.0649  
iprec_at_recall_1.00   all 0.0185  
P_5                    all 0.3592  
P_10                   all 0.3327  
P_15                   all 0.3211  
P_20                   all 0.3082  
P_30                   all 0.2966  
P_100                  all 0.2045  
P_200                  all 0.1446  
P_500                  all 0.0760  
P_1000                 all 0.0399  

#### Method 3
runid                  all myRun  
num_q                  all 49  
num_ret                all 42895  
num_rel                all 2640  
num_rel_ret            all 2188  
map                    all 0.2456  
gm_map                 all 0.1658  
Rprec                  all 0.2746  
bpref                  all 0.2369  
recip_rank             all 0.5625  
iprec_at_recall_0.00   all 0.6165  
iprec_at_recall_0.10   all 0.4681  
iprec_at_recall_0.20   all 0.3848  
iprec_at_recall_0.30   all 0.3260  
iprec_at_recall_0.40   all 0.2947  
iprec_at_recall_0.50   all 0.2538  
iprec_at_recall_0.60   all 0.1998  
iprec_at_recall_0.70   all 0.1667  
iprec_at_recall_0.80   all 0.1241  
iprec_at_recall_0.90   all 0.0748  
iprec_at_recall_1.00   all 0.0201  
P_5                    all 0.3510  
P_10                   all 0.3286  
P_15                   all 0.3238  
P_20                   all 0.3051  
P_30                   all 0.2973  
P_100                  all 0.2057  
P_200                  all 0.1488  
P_500                  all 0.0811  
P_1000                 all 0.0447  