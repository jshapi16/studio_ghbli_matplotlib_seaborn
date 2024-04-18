# studio_ghbli_matplotlib_seaborn
Using a simple studio Ghibli dataset to demonstrate matplotlib and seaborn skills

I downloaded this dataset from <a>https://www.kaggle.com/datasets/shruthiiiee/studio-ghibli-dataset/data</a>. 

I had some questions on the quality of the revenue numbers, so I replaced them manually using figures from <a>https://www.boxofficemojo.com</a>. (Note: many of the most popular movies including Spirited Away and My Neighbor Totoro had multiple release dates. I did not add the revenue together, I only took the revenue from first release. In addition, I filled in missing screenwriter names with the top screenwriter for the project, which was usually the same as the director.

The data needed some cleaning. In particular, I changed the revenue figures from strings to integers, eliminated the "Genre 3" column due to NaNs, changed the "Duration" column to minutes in integers, and removed special characters from the "Name" column (movie title).

Original Dataframe
<img width="1153" alt="original_df" src="https://github.com/jshapi16/studio_ghbli_matplotlib_seaborn/assets/79419060/1d1eea34-9680-4df5-a9d0-930200bb210c">

Clean Dataframe
<img width="1059" alt="clean_df" src="https://github.com/jshapi16/studio_ghbli_matplotlib_seaborn/assets/79419060/0b983087-5738-41bd-b0d5-4aa539fa85b4">

I decided to graph the revenue data visually by movie but there is a large discrepancy between the highest grossing and lowest grossing films, so I created four matplotlib graphs to display the full data and then segmented parts of the data. 

![ghibli_by_revenue](https://github.com/jshapi16/studio_ghbli_matplotlib_seaborn/assets/79419060/4b9e3c16-01f3-4861-bc79-90c3407f044a)


Next I wanted to know whether Studio Ghibli movies generated more revenue over time. To do this, I made two scatterplots plotting year(x) and revenue (y). Two plots because "The Boy and the Heron" generated an outlier amount of additional revenue from the rest of the movies. I plotted the graphs on a logarithmic scale to better see the differences between revenues over time. I annotated each point for ease of viewing and added colors. The lighest colors don't show up as well on the sns darkgrid theme, an additional modification to this graph would be to continue to tweak the colors to better see all the titles. 

![ghibli_revenue_time](https://github.com/jshapi16/studio_ghbli_matplotlib_seaborn/assets/79419060/40025a84-2a70-4d11-af24-5821e2185dc5)


Ultimately, there is no correlation between year and revenue generation. 

To finish the project, I created a dashboard in Tableau with some additional graphs and graphics.
<a>https://public.tableau.com/shared/7K7BCRTT7?:display_count=n&:origin=viz_share_link</a>
