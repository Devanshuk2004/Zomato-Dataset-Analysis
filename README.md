# Zomato API Analysis: Discovering the Best Cuisines Around You

## Context

This project is driven by my fascination with high-quality food served in restaurants and my desire to help the community find the best cuisines around their area. The analysis provides valuable insights for food lovers who want to explore top-notch cuisines within their budget, identify value-for-money restaurants, and locate the best dining spots in various localities.

## Content

**Zomato API Analysis** is an essential resource for food enthusiasts seeking the best cuisines worldwide that fit their budget. This analysis also caters to individuals who want to find value-for-money restaurants in different regions and those eager to discover the top cuisines in specific localities. The project leverages the Zomato API to gather and analyze data, helping users make informed dining decisions.

- For more information on Zomato API and obtaining an API key:
  - Visit: [Zomato API Documentation](https://developers.zomato.com/api#headline1)
  - Data Collection: [Zomato API Data Collection](https://developers.zomato.com/documentation)

## Data

### Fetching the Data

- **Source**: Data was collected from the Zomato API in `.json` format using the following endpoint:
- **Raw Data**: The raw `.json` files collected from the API can be viewed [here](link-to-raw-data).

### Data Storage

The collected data has been stored in a Comma Separated Value file (`Zomato.csv`). Each restaurant in the dataset is uniquely identified by its Restaurant Id. The dataset contains the following variables:

- **Restaurant Id**: Unique identifier for each restaurant across various cities.
- **Restaurant Name**: Name of the restaurant.
- **Country Code**: Country where the restaurant is located.
- **City**: City where the restaurant is located.
- **Address**: Full address of the restaurant.
- **Locality**: Locality within the city.
- **Locality Verbose**: Detailed description of the locality.
- **Longitude**: Longitude coordinate of the restaurant's location.
- **Latitude**: Latitude coordinate of the restaurant's location.
- **Cuisines**: Cuisines offered by the restaurant.
- **Average Cost for Two**: Cost for two people in different currencies.
- **Currency**: Currency used in the country.
- **Has Table Booking**: Yes/No indicating if table booking is available.
- **Has Online Delivery**: Yes/No indicating if online delivery is available.
- **Is Delivering**: Yes/No indicating if the restaurant is currently delivering.
- **Switch to Order Menu**: Yes/No indicating if there is an option to switch to the order menu.
- **Price Range**: Range of prices for food.
- **Aggregate Rating**: Average rating out of 5.
- **Rating Color**: Color representing the average rating.
- **Rating Text**: Textual description based on the rating.
- **Votes**: Number of ratings cast by users.

## Acknowledgements

I would like to express my gratitude to the Zomato API for providing the data that made this analysis possible.

## Inspiration

The data processing for this project focused on the following categories:
- Currency
- City
- Location
- Rating Text

## Work Done

### Data Transformation

- Added a column representing the number of cuisines offered by each restaurant.
- Introduced new columns:
- **HT**: Boolean indicating if the restaurant has table booking.
- **HO**: Boolean indicating if the restaurant has online delivery.
- **ISD**: Boolean indicating if the restaurant is delivering now.
- **SM**: Boolean indicating if the restaurant has the "Switch to Order Menu" option.
- Converted relevant columns to boolean values and removed unnecessary columns.

### Exploratory Data Analysis (EDA)

- Performed `.info()` to understand the dataset structure.
- Created pair plots to explore relationships between ratings and other features.
- Generated box plots to compare ratings against price ranges.
- Constructed a correlation heatmap to visualize relationships between variables.

### Machine Learning

- Split the data into training and testing sets.
- Applied **Linear Regression** to model the data.
- Generated OLS results and model summary to evaluate model performance.

