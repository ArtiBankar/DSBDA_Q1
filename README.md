# DSBDA_Q1
##Datafreame
import pandas as pd
#data = {"Roll-num": [10,20,30,40,50,60,70], "Age":[12,14,13,12,14,13,15], 
"NAME":['John','Camili','Rheana','Joseph','Amanti','Alexa','Siri']}
data = pd.read_csv('dataset_Facebook.csv')
block = pd.DataFrame(data)
print("Original Data frame:\n")
print(block)
print(block.loc[[0,1,3]])
print(block.loc[0:3])
#print(block.loc[0:2,['Age','NAME']])
print(block.loc[0:2,['Type','like']])
print(block.iloc[[0,1,3,6],[0,2]])
##Merging
import pandas as pd
d1 = {'Name': ['Pankaj', 'Meghna', 'Lisa'], 'Country': ['India', 'India', 'USA'], 'Role': ['CEO', 
'CTO', 'CTO']}
df1 = pd.DataFrame(d1)
print('DataFrame 1:\n', df1)
df2 = pd.DataFrame({'ID': [1, 2, 3], 'Name': ['Pankaj', 'Anupam', 'Amit']})
print('DataFrame 2:\n', df2)
df_merged = df1.merge(df2)
print('Result Inner Join:\n', df_merged)
print('Result Left Join:\n', df1.merge(df2, how='left'))
print('Result Right Join:\n', df1.merge(df2, how='right'))
print('Result Outer Join:\n', df1.merge(df2, how='outer'))
