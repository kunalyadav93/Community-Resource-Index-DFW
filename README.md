# Community-Resource-Index-DFW
Processed and analyzed census tract level data of DFW Metroplex to make a Community Resource Index (CRI)
Here is a brief document detailing the methodology taken to go ahead and calculate the Economic Index. 
All data were collected from the United States Census Tract Level for the 4 counties of Dallas, Collin, Tarrant and Denton. 

This data was then used to calculate the Economic Index. Identifying and selecting indicators were a very broad aspect during the early phases and it was done through significant statistical techniques and an understanding of economics-influencing factors from a pragmatic perspective. 
Steps to Calculate the Economic Index 
 
###### 1.	Z transformation 

a.  	Z-Transformation was used to assess the distribution within the variables and transform them.

b.	  It allows us to identify the distribution of variables around their mean.  

c.	Formula :  

![Image description](https://i.postimg.cc/T29MRMc2/formula.png)

###### 2.	Principal Component Analysis (PCA) 

a.	Due to high correlation within the data, PCA was used and not regression. 

b.	Variable clustering was used to cluster the variables based on their correlations. 

![Image description](https://i.postimg.cc/nMb04L49/jpg.png)
 
c.	There were the 3 clusters: 

i.	Cluster 1: Median Household Income and House ownership which are both factors that are related to each other as people with more income are more likely to own a house. 

ii.	Cluster 2: Single Headed Family, Households Receiving SNAP and Households with Public Assistance which are all factors that show poverty in a neighborhood which explains this grouping. 

iii.	Cluster 3: Commute Duration greater than 60 mins, Commute Duration greater than 90 mins and Employment rate are related since as employment rate increases/ decreases, the number of people who commute to their work will also decrease/ increase. 
 

![Image description](https://i.postimg.cc/vmNj1bNf/branch.jpg)
###### 3.	PCA was implemented separately on each cluster and then on the results to obtain the weights that can be used to calculate the final index.  
  
![Image description](https://i.postimg.cc/1R6TtxcV/table.jpg) 
The below formula was used to calculate the Index: 
 
Economic Index = [(Median Household Income*0.7071 + House ownership*0.7071) *0.7071 + (Single Headed Family*0.6028 + Households Receiving SNAP*0.659 + Households with Public Assistance*0.4496) * (-0.7071)]*0.7071 + [(Commute Duration greater than 60 mins*0.7071 + Commute Duration greater than 90 mins*0.7071) *0. 7071+ Employment rate*(-0.7071)] * (-0.7071) 
 
Finally, the calculated index was scaled using min-max scaling to convert it to the range 0 to 100. 
