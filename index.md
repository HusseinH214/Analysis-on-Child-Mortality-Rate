- For this project I was partnered with Serena Li
- The link to the projects code can be found [here](https://github.com/HusseinH214/Analysis-on-Child-Mortality-Rate/blob/main/Final_Project.ipynb)


### Part II of My Report:

For finding a connection between extreme poverty rates and child mortality causes I first started with loading the data into a colab with the idea to merge 
them. Before I could, the dataset containing
the extreme poverty rates had a lot of missing data that I needed to figure out what to do with. I decided to filter past the year 1950 and then drop any missing data from the extreme poverty column.
Next I removed any entries that were duplicates or unneeded. The second dataset containing information on causes of child mortality was completely intact, but due to a limit on exporting I was only able
to get the year up to 2001. With both datasets cleaned I decided to merge the two.

With the datasets merged I was then ready to create a visualization. This was something that stumped me for a while as I was considering the different ways to display data like the extreme poverty rates 
and cause of death rates for each cause of death. This information was gonna be displayed for each country so because of how many parts were involved I settled on categorizing the causes of death from 1-3 
based on how preventable the cause is financially. Each cause was assigned a category which was mapped as a column in the dataframe. This is where I began to face a lot of difficulties with my code. 
For starters, I had originally planned to group countries by region and year, aggregate and average the data for the countries in each region, and then display the regional data. For some reason 
however when I averaged the data the entries, regardless of the year, we’re all the same thing. I couldn’t figure out how to fix this so I ended up downsizing to just one region, had the same issue, 
and ended up just examining a handful of random countries.
For each subplot I planned on making I made a filtered version of the dataframe containing entries relating to one of the 3 categories for causes of deaths. I then tried to play around with adding the 
traces using a for loop to avoid adding them individually but had trouble and eventually just used AI to make it for me. I also decided to make a separate subplot containing the extreme poverty rates 
for comparison. The idea was to compare the categorized causes of death subplots to the extreme poverty 
rates and see if any countries had any correlations.Some of the subplots came out like:


<div style="margin-left: 0; padding-left: 0;">
  <div style="text-align: left;">
    <iframe src="Category1.html" width="49%" height="500" style="border:none; display: inline-block;">
      Your browser does not support iframes.
    </iframe>
    
    <iframe src="Category2.html" width="49%" height="500" style="border:none; display: inline-block;">
      Your browser does not support iframes.
    </iframe>
  </div>
  
  <div style="text-align: left;">
    <iframe src="Category3.html" width="100%" height="500" style="border:none; display: block;">
      Your browser does not support iframes.
    </iframe>
  </div>
  
  <div style="text-align: left;">
    <iframe src="povertyrates.html" width="50%" height="500" style="border:none; display: block;">
      Your browser does not support iframes.
    </iframe>
  </div>
</div>

The way I actually viewed the cause of death subplot and the subplot for the poverty rates was through the use of monitors so I can see them side by side. Some issues I couldn’t really solve with the
United Kingdom’s poverty rate having 0’s where the value just drops and because of the way the time frames line up most of the extreme poverty data past 2000 didn’t line up with the causes of death. 
This has to do with the way the cause of deaths dataframe was exported.
Analyzing the data there was definitely variation in what causes of child mortality have a correlation with the extreme poverty rate of the country. In places like the UK, Canada, and India there seemed 
to be a correlation between the poverty rate and mortality rate for nutritional deficiencies. In some cases like with self harm, neurological disorders, and transport injuries the child mortality rate
didn’t really correlate with a poverty rate, but was somewhat low across all countries. We can see something similar with the STI’s 
death rate all being close for different countries despite differing poverty rates.  With digestive diseases, Mexico, Canada, and India all followed a similar trend of increasing despite having a 
decreasing poverty rate.There were also some causes like unintentional injuries that made me question how it could be related to a country's poverty rate.
 
