# medical_insurance_portfolio_project


The goal of this project was to explore the data in the insurance.csv file, which contains medical insurance costs and relevant information such as age and sex. 

Originally a CSV file, the data is stored in the Jupyter Notebook file for analysis in a set of lists, which are defined and populated near the beginning of the program.

Many functions have been defined within the function for analysis of the data. 

average_value(): 
This function takes a list as input and returns the mean of the elements of the list.

sex_breakdown(): 
This function takes the list of sex data as input and returns the ratio of males to females. This was designed to reveal any biasses in the data based on sex, i.e. overrepresentation of men or women. Calling the function shows that there are slightly more males than females in the data, but the discrepancy is so slight as to be unimportant. Since the only list in the program that this function can be used on is the sex list, the function could have been written without a parameter. The function still has a paremeter, however. 

list_elements():
This function takes any of the lists of the data and returns a list with each element listed only once. This is useful on the region list, because the CSV file is too long to count the different regions manually. 

sort_costs():
This function takes the charges list and one of the other lists as input, and returns a dictionary with the keys being the elements of the second list, and the values being a list of charges corresponding to the keys. For example, used on the region list, this function would return a library with four keys, one for each of the four regions, and the values would be lists of the insurance costs for each of the four regions. 

sorted_averages():
This function takes what sort_costs() returns as output, and returns a dictionary where the keys are the same as the sort_costs() output, but the values are the averages of the elements in the lists that were the values of the sort_costs() output.

find_minimum() and find_maximum():
These functions take the dictionary output of the sorted_averages() function as input, and returns the key that corresponds to the maximum/minimum value as well as the maximum/minimum value.

compile_data():
This function takes the dictionary output of the sorted_averages() function, and returns None, but prints the outputs of the find_maximum/minimum() functions in a somewhat readable format.

analyze_data():
This function takes one of the lists of data as input as well as what that data should be called, such as "Sex" or "Age," and uses many of the other functions to provide some insight into the data. Interestingly, this function does not work on the region list, even though the entire functionality works on the region list when done manually without the analyze_data() function.