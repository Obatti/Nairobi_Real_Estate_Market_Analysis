\# Nairobi Residential Real Estate Market Analysis



An analysis and price prediction project looking at residential property listings across Nairobi.



The goal is to understand what actually drives house and apartment prices in Nairobi, clean up messy scraped listing data, and see how well regression models can predict prices using location and property features.



\---



\## Why I Worked on This



Real estate prices in Nairobi vary a lot depending on where you look. A house in Karen does not follow the same pricing logic as an apartment in Kilimani or Ruaka. Many online listings also have unrealistic asking prices or typos.



I set up this project to check:

\* How much the specific neighborhood affects the price compared to property size.

\* The actual price differences between standalone houses, townhouses, and apartments.

\* Whether basic property details are enough to build a reliable price prediction model.

\* How to give buyers, investors, and property businesses concrete data so they can evaluate deals faster instead of relying on guesswork or inflated listing quotes.

\* How to spot mispriced or undervalued listings in high-demand estates before making an offer or financing a project.



\---



\## The Data



The dataset contains residential property listings scraped from Property24 Kenya.



\### Key Details in the Data

\* \*\*Location:\*\* The neighborhood or area (such as Kilimani, Westlands, Karen, Kileleshwa).

\* \*\*Property Type:\*\* House, Townhouse, or Apartment.

\* \*\*Bedrooms:\*\* Number of bedrooms.

\* \*\*Bathrooms:\*\* Number of bathrooms.

\* \*\*Price:\*\* Asking price in Kenya Shillings (KES).



\---



\## Project Steps



\### 1. Cleaning the Data

\* Converted price text into numbers in KES.

\* Checked and filled missing values for rooms and locations.

\* Removed extreme price errors and outliers that would throw off the models.

\* Handled skewed price figures so the regression models could read patterns properly.



\### 2. Exploratory Analysis

\* Looked at median prices across different estates and suburbs.

\* Compared how prices change when moving from apartments to standalone houses.

\* Checked how much an extra bedroom or bathroom actually adds to the total price.



\### 3. Model Training

\* Ran linear and non-linear regression models to test how accurately they estimate prices.

\* Compared predictions against real asking prices using standard error metrics.



\---



\## What the Data Shows



\* \*\*Location is the main price driver:\*\* Moving a house to a different neighborhood changes its price far more than adding another room.

\* \*\*Apartments have tighter price ranges:\*\* Apartment pricing is fairly consistent, while standalone houses have wide price spreads because of compound size and land value.

\* \*\*Extra rooms stop adding value after a point:\*\* Adding bedrooms increases the price up to about 3 or 4 bedrooms. Past that, the price depends more on the area and land size than room count.



\---



\## Model Limitations and Challenges



\* \*\*Asking prices vs. actual closing prices:\*\* The model is trained on online listing figures from Property24, which often include seller markups or room for negotiation. These may not reflect the actual final transaction prices agreed at closing.

\* \*\*Missing land size and plinth area:\*\* Online listings frequently leave out total acreage or square footage. Without exact land sizes, valuation for standalone houses and townhouses has an unavoidable margin of error.

\* \*\*Unstructured qualitative details:\*\* Value drivers like interior finishes, backup generators, borehole access, and compound security are buried in unstructured text descriptions rather than standardized data columns.

\* \*\*Spatial granularity:\*\* Listings often group broad areas together (e.g., "Westlands" or "Kilimani") without exact street coordinates, missing out on hyper-local price differences within the same neighborhood.



\---



\## Future Improvements



\* \*\*Incorporate physical property dimensions:\*\* Collecting consistent square meter measurements and parcel sizes will substantially reduce valuation errors on landed properties.

\* \*\*Extract text features using NLP:\*\* Parsing listing descriptions to capture high-value amenities (such as swimming pools, fitted kitchens, or solar power) as explicit categorical variables.

\* \*\*Integrate geospatial coordinates:\*\* Using exact latitude and longitude data to map proximity to key road corridors, business districts, and social infrastructure.

\* \*\*Model experimentation:\*\* Moving from baseline models to tuned gradient boosting algorithms (such as XGBoost or LightGBM) to better capture complex interactions between location and home specs.



\## Project Setup



```text

├── notebooks/

│   ├── 01\_nairobi\_housing\_eda.ipynb   # Notebook containing all code, plots, and models

│   └── requirements.txt              # Required Python packages

├── .gitignore                        # Files to ignore in Git

└── README.md                         # Project notes and documentation

