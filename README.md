# Busiest-Airports-Web-Scraping
This is a project i built to apply the concepts of data collection using web scraping, data pre-processing and data visulization learnt in the subject of 'Conversational AI Basics' taught at my university.
The project broadly consist of 2 steps:
## DATA COLLECTION
In this project, we employ the BeautifulSoup Python package as our web scraping tool to extract valuable data from the Wikipedia page List of the busiest airports in India. This page presents a comprehensive ranking of airports in India based on critical parameters, as officially published by the Airports Authority of India. The ranking criteria encompass total passenger traffic (in persons), which accounts for arrivals, departures, and transit passengers at each airport. Additionally, the ranking considers total aircraft movements (in aeroplane times), covering all takeoffs and landings of various aircraft in scheduled or charter conditions. Finally, the total cargo handled (in metric tonnes) is crucial, encompassing all freight and mail that arrives at or departs from each airport.
The BeautifulSoup parser is instrumental in navigating and extracting information from these tables. It systematically traverses the HTML structure, locates relevant table elements, and captures the data according to the specified fields. By integrating BeautifulSoup, this project streamlines the process of gathering and organizing airport-related statistics. The extracted data, stored in a structured format, facilitates further analysis, providing valuable insights into the busiest airports in India based on passenger traffic, aircraft movements, and cargo handling. This approach ensures the accurate representation of airport rankings and supports informed decision-making in the realm of aviation.

## DATA PRE-PROCESSING
Data pre-processing is a critical step in preparing raw data for analysis, and in this context, it involves extracting and transforming tabular information from an HTML table. The table is structured with specific column headings: Rank, Name, City, State/UT, IATA Code, Passengers in 2022-23, Passengers in 2021-22, %change, and Rank Change. Each row of the HTML table is treated as an individual record and is meticulously processed to form a Pandas DataFrame, a versatile data structure in Python for data manipulation and analysis.
For every row in the HTML table, the script employs the BeautifulSoup library to locate all table data (<td> elements). The text content of each of these elements is then extracted and compiled into a list named individual_row_data, capturing the details corresponding to each column heading. Subsequently, the script appends a new row to the Pandas DataFrame (df) with an index determined by the current length of the DataFrame. This dynamic indexing ensures the seamless integration of each row of data into the data frame.
The resulting Pandas data frame is a well-organized repository of the tabular information, enabling easy exploration and analysis of the extracted data. To facilitate further data utilization, the script concludes by converting these Pandas data frames into a CSV (Comma-Separated Values) file using the df.to_csv method. The CSV file preserves the original column headings, providing a clear and structured representation of the tabular data conducive to subsequent analysis, visualization, and reporting. This meticulous process streamlines the data from its raw HTML form into a format accessible and amenable to a wide range of analytical tasks.
