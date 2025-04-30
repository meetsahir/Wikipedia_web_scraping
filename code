#In this project we are extracting data from a table present in Wikipedia webpage
#The data will be extracted from the table and placed in a dataframe
#This data can then be saved in a .csv file or Excel file for further analysis or we can use pandas to analysis the data in Python

#importing the required libraries
import requests
from bs4 import BeautifulSoup
import pandas as pd

pd.set_option('display.max_rows', None)               #setting option to display all rows
pd.set_option('display.max_columns', None)            #setting option to display all columns
url = "https://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population"
page = requests.get(url)
#print(page)          --- checking the response from the url which is 200 so good to go

soup = BeautifulSoup(page.text, "html.parser")
#print(soup)          ---- reading the text from the url, which is done successfully

table = soup.find("table", class_ = "wikitable sortable mw-datatable sort-under static-row-numbers sticky-header col1left col5left")
#print(table)         ---- finding the table from which we need to capture the data

table_titles = table.find_all("th")
#print(table_titles)   ---- extracting all the 'th' tags from the tables which are the table headers

population_table_titles = [title.text.strip() for title in table_titles]
#print(population_table_titles)          ---- extracting the header texts from the 'th' tags

df = pd.DataFrame(columns= population_table_titles)
#print(df)                   ---- populating the extracted texts as column names of the dataframe

rows = table.find_all("tr")
for row in rows[1:]:
    cells = row.find_all("td")
    row_data = [cell.text.strip() for cell in cells]
    #print(row_data)         ---- looping the 'tr' tags which are table rows and extracting the text from 'td' tags which is table data

    length = len(df)                #  --- finding out the length of the dataframe
    df.loc[length] = row_data       # ---- putting the extracted data to the length of the dataframe

 print(df)                           # ----- printing the dataframe
