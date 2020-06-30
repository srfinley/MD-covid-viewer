# Local Maryland COVID-19 Visualizers

## Why this?

Like a lot of people in self-isolation, my dad has made "checking coronavirus stats for his local area" a part of his daily routine. The [Maryland COVID-19 dashboard](https://coronavirus.maryland.gov/) is an excellent resource, including highly granular views at the county and zip code level.

But those granular views aren't available over time; for the sub-state regions, it's only possible to get that day's cumulative snapshot. To help my dad see the overall trajectory of the virus's spread, I produced a pair of Python notebooks he could use to visualize both cumulative cases and the rolling average of new cases per day by county and zip code.

## How to use

If you've used notebooks locally before and would prefer to go that route, just make sure your Python environment includes the following dependencies:

- pandas
- requests

But this is how my dad does it:

1. Open the desired notebook in Colab. From GitHub, you can do this by clicking the "Open in Colab" button at the top of the notebook. If you do not prefer to have your own local copy of the code that retains changes, skip to step 4.
2. Make a copy of the notebook in your Google Drive storage. In the page header, go to File -> Save a Copy in Drive. You'll have to be logged into your Google account for this to work.
3. The copy should pop up in a new window or tab. You'll know it's your own personal version because the title in the page header will be "Copy of ___.ipynb". Now you can run the code and change the variables to look at whichever zip codes or counties you're interested in.
4. Run each code cell sequentially, from top to bottom. The "[  ]" at the top left corner of every gray block is where you click to run it (mousing over it will reveal a circular "play" icon). Read the comments inside the code cell to better understand what's happening inside it. Keep in mind that the first cell in particular might take a little while to run.
5. There are a few variables you can change to customize your view of the data. Both visualizations accept lists of regions to display, and the "rolling average" chart will accept a number of days over which to average the number of new cases. To generate a fresh visualization based on these variables, you'll have to run the cell into which you just input the variable.

## The Future

The notebook format represents a compromise between ease of use and ease of creation. This tool was initially envisioned as an online dashboard like the official Maryland source, and I may still end up putting in the additional work to create that, schedule permitting.

## APIs

The data sources for the visualizations come from coronavirus.maryland.gov. Check them out for yourself [here (for zip code)](https://coronavirus.maryland.gov/datasets/mdcovid19-master-zip-code-cases) and [here (for county)](https://coronavirus.maryland.gov/datasets/mdcovid19-casesbycounty).
