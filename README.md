
# Web Scraping 

In this project we are scraping data from a website(Wikipedia) fir further analysis 

# Description
We are scraping the population data of world from Wikipedia which will be used for further analysis 

The data is stored within a table in the website which we will be pulling into a dataframe

We are using Python to complete this project

![Image](https://github.com/user-attachments/assets/ac4d3e4e-4de0-471c-a7bb-0b0f7cc63cc6)

# Steps involved
1. We will first import the required libraries - requests, BeautifulSoup and pandas 

![Image](https://github.com/user-attachments/assets/3de62d09-fafd-4e6f-a40b-e039edfa2470)

2. Next we will check if data can be pulled from the website or not, we write the query and get a response 200, which indicates that data can be pulled from the website

![Image](https://github.com/user-attachments/assets/4835c96a-ab5f-42c9-901d-c553d53a019a)

3. Next we pull the complete data from the website and find the table that contains the data we want 

![Image](https://github.com/user-attachments/assets/c06b5c06-283d-405a-a4ef-68495b4d1299)

4. Next we find the table headers which are contained in the 'th' tag and add them as columns in the dataframe

![Image](https://github.com/user-attachments/assets/3c54f2b1-3ba7-4348-b11f-fadb2cdef10b)

5. Finally we find the table rows whihc are contained under the tag 'tr', loop through them to find the actual data which stored under table data 'td' tag. Once the values are extracted, we add them to the dataframe to get the desired result

![Image](https://github.com/user-attachments/assets/d1933c92-9a5a-4d23-9ef1-6afe507d76b0)

#Conclusion
We are able to achieve the desired result by extracting the data from the table in the website to the dataframe. This data can now to moved further into a .csv file or Excel for further analysis or we can even analyze the dataframe further for finding meaningful insights
