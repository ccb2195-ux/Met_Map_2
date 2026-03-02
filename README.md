# Mapping the Met's Collection

**Idea: Take the open source Met collection database, scrape it into a CSV, and use that CSV to tell a story of the geography behind the MET's collection.**

*The geography data was spare to begin with and I experimented with Regex to clean it so this dataset SHOULD NOT BE TRUSTED to be 100% geographically accurate*

-> Findings:
- Most of the Met's collection by volume comes from Egypt.
- The Met's American Collection comes largly from one guy named Jefferson R. Burdick, an enginner from Syracuse, who donated almost 30,000 baseball cards
- The Met's largest purcahsing fund comes from one man, Jacob S. Rogers, a train tycoon from the late 1800s who is vastly understudied compared to his other giled age counterparts like Rockefeller or Morgan. 

-> Goals/Proccess:
- After getting access to the Met's large open dataset, I cleaned the country data by having Claude Code help me make regex statments to correct spelling, country naming, and approximation errors.
- From there I made two visualizations, a stacked bar chart showing the top 5 major gifts to the mueseum and where those  came from, as well as a geographic visuialization of all the pieces that have location data associated.
- I used Jsoma's basic website template to create the index.html file and I formated most of the rest of the HTML bby myself, with the expection of the red line at the top of the page, for which I employed Claude Code
- I interviewed four random passer-bys at the Brooklyn Mueseum about how they felt around where the artifacts came from ans who paid for them, only one of which made it into the story.
- My final product of analysis is in the donor_country_pivot_sorted.csv which contains my cleaned country data sorted by the gift/credit_line data from the original dataset.

-> Limitations/Challenges:
- I quickly ran into issues with the Met API so I imediatly pivoted to the same data set in the form of a github repo (METopenaccess).
- The Met files where in gitlfs format which I had never seen before.
- The Met's data has very limited geographic information, with only 16% of the ~400,000 piece collection having any geography data at all
- The geography data that does exist in the Met data set has a plethora for problems including spelling errors and approximate statmentes (ex. Maybe Egypt?).
- I didn't start reaching out to sources soon enough and got chewed out by the Met's Head of Curation for calling/emailing her team over the weekend.
- I experamented with many different methods of data cleaning and visualization, but the main dataset I use for the final visualization was cleaned in MET_map_explore.ipynb, Met_country_cleaned_explore.ipynb and credit_line_explore.ipynb.
