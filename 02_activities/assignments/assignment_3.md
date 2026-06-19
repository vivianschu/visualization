# Data Visualization

## Assignment 3: Final Project

### Requirements:
- We will finish this class by giving you the chance to use what you have learned in a practical context, by creating data visualizations from raw data. 
- Choose a dataset of interest from the [City of Toronto’s Open Data Portal](https://www.toronto.ca/city-government/data-research-maps/open-data/) or [Ontario’s Open Data Catalogue](https://data.ontario.ca/). 
- Using Python and one other data visualization software (Excel or free alternative, Tableau Public, any other tool you prefer), create two distinct visualizations from your dataset of choice.  
- For each visualization, describe and justify: 
    > What software did you use to create your data visualization?

    > Who is your intended audience? 
    
    > What information or message are you trying to convey with your visualization? 
    
    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
    
    > How did you ensure that your data visualization is accessible?  
    
    > Who are the individuals and communities who might be impacted by your visualization?  
    
    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 
    
    > What ‘underwater labour’ contributed to your final data visualization product?

- This assignment is intentionally open-ended - you are free to create static or dynamic data visualizations, maps, or whatever form of data visualization you think best communicates your information to your audience of choice! 
- Total word count should not exceed **(as a maximum) 1000 words** 

### Plot 1: Average E.coli Levels by Beach (Bar Chart)
> What software did you use to create your data visualization?

I used python, pandas and matplotlib to create this data visualization.

> Who is your intended audience? 

The intended audience would be Toronto residents who want a quick and accessible summary of water safety conditions across city beaches during the summer swimming season. It could also be helpful for public health communicators or city staff who need to present safety data clearly.

> What information or message are you trying to convey with your visualization? 

The main message is which Toronto beaches had the highest and lowest average E. coli concentrations during Summer 2023, relative to the provincial safety threshold of 100 CFU per 100 mL. The ranked comparison helpes the audience identify which beaches are generally safest and which need closer monitoring/caution.

> What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 

Attributes/Color: I used teal for beaches whose seasonal average falls below the safety threshold and orange for those above it (cool = safe, warm = caution). This is also distinguishable for those with a color deficioency, avoiding red/green pairings.
Reference Line: The dashed red veritcal line marks the 100 CFU/100mL threshold which anchors each bar in a safety context. This reduces the need for the reader to mentally compare absolute values.
Sorting: Bars are sorted by average E.coli, making the rank order readable without the reader having to scale up and down the y-axis to compare values.

> How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 

The code is included in [a3_plot.ipynb](a3_plot.ipynb).

> How did you ensure that your data visualization is accessible?  

- Contrast against white background
- Tet size labels >=9 pt and title is 13pt
- Bars are sorted, so color and position carries the same information

> Who are the individuals and communities who might be impacted by your visualization?  

Toronto residents who use city beaches for recreation are most impacted by my visualization. Young children, elderly residents, immunocompromised individuals, etc. who face greater health risk from elevated E.coli exposure would be the most directly impacted. Communities near beaches may have different access patterns. 

> How did you choose which features of your chosen dataset to include or exclude from your visualization? 

The dataset includes beach name, sample date, E.coli count, beach status (safe/unsafe). For Visualization 1, individual sample dates were aggregated to a single seasonal average per beach to reduce noise and communicate the overall pattern. The "Beach Status" categorical column was excluded in favour of computing the comparison against the threshold directly from the numeric counts, which is more precise.

> What ‘underwater labour’ contributed to your final data visualization product?

- Researching the dataset on the City of Toronto Open Data Portal and verifying the provincial E. coli threshold used to classify swimming safety.
- Iterating on bar colour choices to ensure accessibility for colour vision deficiency
- Removing default matplotlib styling (spines, tick marks) to reduce visual clutter
- Writing and testing the data aggregation code to ensure the groupby operation produced the correct per-beach means
- Choosing and justifying the sort order to best serve the audience's likely question ("which beach is safest?")

### Plot 2: Weekly E.coli Levels Over Time (Line Chart)

> What software did you use to create your data visualization?

Microsoft Excel. CSV was imported directly and a line chart was created using Insert > Chart with "Date" as the x-axis and E.coli count as the y-axis.

> Who is your intended audience? 

Public health staff or city analysts who need to track beach safety trends across the summer season. This audience is comfortable with time-series charts and needs to identify whether dangerous E. coli spikes are isolated events (e.g., post-rainfall) or sustained patterns requiring extended beach closures.

> What information or message are you trying to convey with your visualization? 

The chart shows how E. coli levels fluctuate week-to-week at three selected Toronto beaches (Woodbine, Sunnyside, Cherry Beach) throughout Summer 2023. The message is temporal showing that water quality is not static but rather it spikes and recovers.

> What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 

- Line charts leverage the human visual system's tendency to perceive connected points as a continuous trend, making them well-suited for time-series data
- Three distinct, high-contrast hues were used for the three beach lines (dark teal, gold and orange-red) to allow simultaneous comparison without relying on a single dimension
- Only three beaches were included (out of eight) to avoid overplotting and maintain legibility

> How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 

Microsoft Sheets is not fully reproducible in the way code is: the chart depends on the user's manual steps in the GUI. To mitigate this:
- The same CSV (toronto_beaches_water_quality.csv) used in Visualization 1 is the input, so the data is consistent
- Added [a3_plot2.xlsx](a3_plot2.xlsx) with the raw data and chart for reference, so the process can be replicated manually if needed

> How did you ensure that your data visualization is accessible?  

- Each beach line uses a distinct colour and marker shape (circle markers), so the series can be distinguished by shape alone if colour is unavailable
- All text is 9 pt or larger; the title is 13 pt.
- The teal/gold/orange-red palette avoids the red/green pairing that fails for red-green colour blindness

> Who are the individuals and communities who might be impacted by your visualization?  

The same beachgoing communities mentioned in Visualization 1 apply here. Additionally, because this chart highlights specific time periods when beaches exceeded the safety threshold, it could affect how the public perceives individual beaches' overall reputation. 

> How did you choose which features of your chosen dataset to include or exclude from your visualization? 

From the dataset's columns (Beach Name, Date, E. coli Count, Beach Status), the time dimension (Date) and the numerical measurement (E. coli Count) were needed for this chart. Only three of eight beaches were included to avoid an overplotted, unreadable chart (Woodbine, Sunnyside, and Cherry Beach).

> What ‘underwater labour’ contributed to your final data visualization product?

- Evaluating whether a line chart, area chart, or small multiples would best serve the time-series goal
- Selecting a three-beach subset
- Testing the colour palette for colour vision deficiency
 
### Why am I doing this assignment?:  
- This ongoing assignment ensures active participation in the course, and assesses the learning outcomes: 
* Create and customize data visualizations from start to finish in Python
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story  
- This would be a great project to include in your GitHub Portfolio – put in the effort to make it something worthy of showing prospective employers!

### Rubric:

| Component         | Scoring  | Requirement                                                                 |
|-------------------|----------|-----------------------------------------------------------------------------|
| Data Visualizations | Complete/Incomplete | - Data visualizations are distinct from each other<br>- Data visualizations are clearly identified<br>- Different sources/rationales (text with two images of data, if visualizations are labeled)<br>- High-quality visuals (high resolution and clear data)<br>- Data visualizations follow best practices of accessibility |
| Written Explanations | Complete/Incomplete | - All questions from assignment description are answered for each visualization<br>- Explanations are supported by course content or scholarly sources, where needed |
| Code              | Complete/Incomplete | - All code is included as an appendix with your final submissions<br>- Code is clearly commented and reproducible |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 -  2026-06-16`
* The branch name for your repo should be: `assignment-3`
* What to submit for this assignment:
    * A folder/directory containing:
        * Two distinct data visualizations (for example, PNGs, PDFs, or screenshots)
        * Two Markdown files answering all questions for each visualization (including a link to your dataset in both files)
        * One Python file contains the complete code and visualization, and another file (with or without code) contains the visualization.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-3`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
