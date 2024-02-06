# Module 12 Challenge
## MongoDB

This repository focuses on food hygiene ratings from the UK Food Standards Agency.  The database is being prepared for the magazine "Eat Safe, Love" to help them determine restaurants they would be interested in writing about.  

Ratings information was imported from a JSON file named [establishments.json] located in this repository's 'Resources' folder.  The database was named 'uk_food' and the collection was named 'establishments'.  

### Database Preparation for Analysis
Within the jupyter notebook file [NoSQL_setup_starter](NoSQL_setup_starter.ipynb) PyMongo was utilized to edit the uk_food database.  Additional restaurant information for the business "Panang Flavours" was manually added to the database and updated with current information. Documents were removed for the 'Dover' local authority, as this region is not of interest to "Eat Safe, Love". Values for "latitude" and "longitude" were converted to floats, and the "RatingValue" was converted to integer.  

### Exploratory Analysis
The code in jupyter notebook file [NoSQL_analysis_starter](NoSQL_analysis_starter.ipynb) produces four separate dataframes from queries of the uk_food database:
1. Establishments with hygiene score of 20.
2. Establishments in London with RatingValue greater than or equal to 4.
3. Top 5 establishments with RatingValue of 5, nearest to the restaurant "Panang Flavours", sorted in ascending order by hygiene score.
4. Counts of the number of establishments by Local Authority that have a hygiene score of 0, sorted from highest to lowest.
