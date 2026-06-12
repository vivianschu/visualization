# Data Visualization

## Assignment 2: Good and Bad Data Visualization

### Requirements:

- Data visualizations are important tools for communication and convincing; we need to be able to evaluate the ways that data are presented in visual form to be critical consumers of information 
- To test your evaluation skills, locate two public data visualizations online, one good and one bad  
    - You can find data visualizations at https://public.tableau.com/app/discover or https://datavizproject.com/, or anywhere else you like! 
- For each visualization (good and bad):  
    - Explain (with reference to material covered up to date, along with readings and other scholarly sources, as needed) why you classified that visualization the way you did.
    ```
    ####
    Bad example
    ####
    Source: https://public.tableau.com/app/profile/vivien.lee88/viz/Formula1ConstructorsRadialBumpChart/Dashboard1

    This visualization is a radial bump chart showing Formula 1 constructors from 2006-2025. It shows how different teams changed ranking or position over time. 

    Font size and color: The title is large and easy to read and the background makes the chart visually interested. However, it also uses many bright coloured lines which makes it difficult to follow one constructor across the full time period. Some times may have similar colors, so viewers have to keep looking back at the legend. This makes the chart less accessible, especially with people with color vision difficulties.

    Layout: The radial layout is creative, but makes the data harder to understand. The years are arranged in a circle and the viewer has to rotate their attention around the chart, making it difficult to compare changes across years. 

    Visual encoding: The chart uses position and line movement to change ove time, but the circular shape distorts comparing positions. Lines cross often and some overlap in the middle of the chart, creating visual clutter. 

    Data interpretation: The visualization does not explain what the lien positions represent and is not immediately clear whether the chart shows constructor ranking, points, championship position, or another measure. The note also says only said only the Top 10 teams are shown but may confused viewers because not all constructors are represented equally across years. 

    ####
    Good Example
    ####
    Source: https://public.tableau.com/app/profile/harim.jung/viz/GlobalCODashboardPoweredbyTableauAgent/TableauAgentClimateDashboard

    This visualization is an AI-powered climate change dashboard that focuses on South Korea’s CO2 emissions. It shows several measures, including CO2 global share, cumulative CO2 share, CO2 per capita, CO2 per GDP, and total CO2 emissions.

    Font size and color: The dashboard uses clear font sizes and strong contrast between text and background. The dark title bar separates the heading from the rest of the dashboard. The colors are also meaningful because they group countries by income level helping the user to understand patterns without needing too much explanation. 

    Layout: The layout is clean and organized. The large "Cumulative Carbon Clock" on the left gives the viewer a main visual focus, while the smaller charts on the right provide supporting  details. This is a clear visual hierarchy where the viewer can first understand overall CO2 pattern then look at specific indicators.

    Visual encoding: The bubble chart compares CO2 per GDP and CO2 per capita and the smaller line plots show changes over time. The chart types match the kind of comparison being made.

    Interactivity: The dashboard lets the user select a country and year. In this case, South Korea is selected and clearly labelled in the bubble chart for the broader global comparison.
    
    Reference: course lecture - cognitive load (intrinsic, extraneous), aesthetic
    ```
    - How could this data visualization have been improved?  
      ```
      ####
      Bad Example
      ####
      The Formula 1 radial bump chart could be improved by using a standard horizontal bump chart instead of a circular layout. This would make it easier to compare teams across years from left to right. The author could also reduce the number of colours or directly label the lines so viewers do not have to keep checking the legend. The chart should clearly explain what the line position means, such as constructor ranking, points, or championship position.

      ####
      Good Example
      ####
      The CO2 dashboard could be improved by adding more short annotations to explain the main findings, such as why South Korea’s emissions changed between selected years. It could also make accessibility stronger by not relying only on colour to show income groups. The dashboard could also more clearly explain the difference between total CO2 emissions and CO2 per capita.
      ```
- Word count should not exceed (as a maximum) 500 words for each visualization (i.e. 
300 words for your good example and 500 for your bad example)

### Why am I doing this assignment?:

- This assignment ensures active participation in the course, and assesses the learning outcomes
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story

### Rubric:

| Component               | Scoring   | Requirement                                                 |
|-------------------------|-----------|-------------------------------------------------------------|
| Data viz classification and justification | Complete/Incomplete | - Data viz are clearly classified as good or bad<br />- At least three reasons for each classification are provided<br />- Reasoning is supported by course content or scholarly sources |
| Suggested improvements  | Complete/Incomplete | - At least two suggestions for improvement<br />- Suggestions are supported by course content or scholarly sources |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 -  2026-06-09`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (assignment_2.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
