# Capstone-Project

## Links to specific stages of the project
1. [Scraping](https://github.com/noahbernstein/Capstone-Project/blob/master/Scraping.ipynb)
2. [Cleaning](https://github.com/noahbernstein/Capstone-Project/blob/master/Cleaning.ipynb)
3. [EDA](https://github.com/noahbernstein/Capstone-Project/blob/master/EDA.ipynb)
4. [Modelling](https://github.com/noahbernstein/Capstone-Project/blob/master/Modelling.ipynb)

## Goals of the project
To see whether it would be possible to accurately predict the price of Airbnb listings, with the idea of being used to guide pricing for Airbnb hosts.

## Why I created the project
I loved scraping when I first learned it, and so wanted to test myself with a harder challenge. I am also a keen Airbnb user, and wondered how hosts first price their listing, either via trial and error or research, in order to come to a fair price. Therefore, I combined the two, and came up with this project.

## Methodology and approach
I scraped the Airbnb website using Selenium, gathering information such as reviews, rating, and a target of price. I then cleaned the data, engineering several different features. Finally, I predicted the price (per night), using regression models, with a focus on using NLP on the reviews that people have left.

## Results
I found that the best model used was the Gradient Boosting Regressor, which yielded a score of 0.706, whilst the most important coefficients were the number of guests, beds, and different bigrams within the reviews. The largest coefficients within the reviews were 'quick helpful', 'comfortable beds', and 'amazing hospitality', which gives hosts an idea of what the qualities are that people look for, which correspond to a higher price.

## Observations and improvements
### Approach
Scraping Airbnb was very challenging, for several different reasons. Firstly, the layout of the website changes every couple of weeks. This meant that if all the scraping wasn't done within a short window, the datasets would vary (eg. at one point, information on number of amenities was present on the page, and other times it wasn't). It also meant that I couldn't get all the information I initially wanted for each listing, but this is something that can be improved upon with more time. Secondly, Selenium was challenging to use, one reason being that it takes a lot of time, since it mimics user actions.

### Data
Although I had enough data to use for modelling, increasing the volume of data is always helpful, and would improve the accuracy of the results. This can be done with more time, and is something I will look into doing.

### NLP approaches
Whilst I used TF-IDF vectorisation, which was successful in highlighting the differences in reviews, there are several more nuances methods of text analysis that I intend to use at some point, but did not get the chance to fully explore.
