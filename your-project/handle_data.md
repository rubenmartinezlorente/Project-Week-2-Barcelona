import pandas as pd

##########################################################################################


#'/Users/rubenmartinezlorente/data-bcn-prework/DATA_COURSE/PROJECTS/P2_Barcelona/Project-Week-2-Barcelona/datasets/3.-Population/births.csv')
##files to read

birth = pd.read_csv('../Project-Week-2-Barcelona/datasets/3.-Population/births.csv')
death = pd.read_csv('../Project-Week-2-Barcelona/datasets/3.-Population/deaths.csv')
population = pd.read_csv('../Project-Week-2-Barcelona/datasets/3.-Population/population.csv')
babies = pd.read_csv('../Project-Week-2-Barcelona/datasets/3.-Population/most-frequent-baby-names.csv')
names = pd.read_csv('../Project-Week-2-Barcelona/datasets/3.-Population/most-frequent-names.csv')

##########################################################################################


##########HOW TO EXTRACT INFORMATION


#d_condition_2015_DC2 = death.loc[(death.Year == 2015) & (death['District.Code'] == 2)]         ##impose two conditions to search

#d_group_age = d_condition_2015_DC2.groupby('Age').sum()         ##group by the attiribute we want, with functions to compact data (one to many) 
#d_deaths_age = d_group_age.loc[:,'Number']                     ##choose which columns wants to show, besides the index(the one grouped by)

#d_deaths_age

#death.loc[(death.Year == 2015) & (death['District.Code'] == 2)].groupby(['Age','District.Name']).sum().loc[:,['Number']]  



##########################################################################################


index_lst[9] = '05-09'

eixample_2015.sort_index()


deaths_2017.groupby(level=[0,1], group_keys=False).apply(lambda group: group.sort_values('Number', ascending=False))

deaths_2017.groupby(level=['District Name','Year'], group_keys=False).apply(lambda group: group.nlargest(1, 'Number'))
