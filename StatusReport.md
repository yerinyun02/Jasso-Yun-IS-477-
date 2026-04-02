# Updates
Our main tasks for this milestone of the project were to import the datasets, clean the datasets, properly structure the datasets for a merge, and merge them. 

Beginning with the imports and cleaning, we both use OpenRefine and VSCode to explore the data. Both datasets were excel files, so we wanted to ensure that we properly imported the data to account for messy layered headers. On OpenRefine, we were able to check that columns were correctly formatted and that the cell values were consistent as far as data types and spelling. 

Once we were confident on the data structure, we each imported our respective dataframes to VSCode to continue deeper cleaning and reformat the datasets where needed. The EIA-860 dataset was clean off the bat, so Yerin and I worked together on the EIA-861 dataset to talk through decisions. The EIA-861 dataset had layered headers that we wanted to flatten to make future analysis easier, so we ultimately decided to transform the data into long format by creating a Sector column. 

Our next step was to prepare the datasets for a merge, so after much discussion and review of our research questions, we decided to structure the EIA-860 dataset on Year-State combos and the EIA-861 dataset on Year-State-Sector combos. 

Our final update for this milestone was merging the datasets and calculating the necessary columns needed to address the research questions. We merged on Year and State, renamed columns were needed, and finally calculated the Use_per_Customer, IPP_Share, Renewable_Capacity, Renewable_Share, Fossil_Capacity, and Fossil_Share. The clean csv’s and final merged dataframe were all pushed to GitHub.


# Updated Timeline

# Changes to Plan

# Challenges Encountered
We continuously referred back to our Project Plan throughout this milestone and as we worked on the datasets, we began to encounter many challenges. Our first challenge was deciding how to format the EIA-861 dataset, which had layered headers. Since our plan was to work on the project using Python on VSCode, we knew reading in the multi-layered data would not be suitable for analysis. We were stuck between keeping the original format, with many columns for all the sector-money combinations, or transforming the data to long format by creating a “Sector” column. After much discussion, we decided that the long format would be easier to interpret and work with in future analysis.

The next challenge we faced was figuring out how to address the null/missing values in the dataset. There were 7 rows with null values for Fuel Type and 1 row with a null value for Summer Capacity (Megawatts). After reviewing the schema, we concluded that we did not have enough information to fill the missing values, and since they were only a small portion of the data, we ultimately dropped the 8 columns with missing values. 

The final and biggest challenge we faced was merging our data. In our original plan, we intended to organize the data as State-Year and State-Year-Fuel Type. However, upon further inspection of our data and as a result of our previous choices in setting up the data, we found that the State-Year and State-Year-Sector was most suitable. 

For all of these challenges, our go-to problem solving strategy was referring back to the Project Plan. Not only did the Project Plan include detailed steps to help break down any issues we were facing, but it also contained the research questions which are the main objective and idea to keep in mind throughout this project. We worked on this part of the project together in person, which really helped with communication and discussing our thoughts. That discussion worked in our favor and we worked very well together on this portion!

# Contribution Summary - Brisa Jasso (bjass2)
My contributions to this project were importing and cleaning the EIA-861 dataset and doing the coding portions of the structuring and merging on my computer. Yerin and I worked together in person for this portion of the project, so a lot of my contributions were alongside discussions to see how we wanted to proceed on each step of the project. Since the code was done on my computer, I also uploaded our final dataframe to GitHub.

# Contribution Summary - Yerin Yun (yryun2)
