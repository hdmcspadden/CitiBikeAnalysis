# Citi Bike Usage in New York City
## Big Data Systems (DS 5110)
**August 11, 2021**

Diana McSpadden (hdm5s)

Nick Daniello (njd9e)

David Fuentes (dmf4ns)

Eric Sarani (es5cj)

Abigail Bernhardt (aeb4rv)

## REPO CONTENTS
* Code_HTML: html version of ipynb files
* Code_IPYNB: python notebooks
* EDA_Images: EDA plots required for course final project
* Presentation: PDF version of slides used for 7-minute final presentation
* Report_ReportAndAppendix: PDF of report sumitted for course and supporting Appendices

** Data used was stored on UVa's High Performance Computing environment, Rivanna (/ds5559/Summer2021_TeamBike).

## ABSTRACT
New York City (NYC) offers residents and visitors a multitude of transportation options, but they must consider numerous factors when deciding which option to use. For this analysis we obtained data from Lyft’s Citigroup-sponsored bike-share program, Citi Bike. By analyzing bike trips between 2018 and 2021, we discovered how changing conditions affect bike usage and how bike usage affects the city. Variables studied included bike-trip specifics (date-time, location, distance), weather, and real estate metrics (zip code, price, etc.). By employing K-Means, Graph Neural Network, Random Forest, Logistic and Linear Regression models, we observed:

1.	Most Citi Bike trips start and end in the same neighborhood, indicating customers use Citi Bike for short trips, or to augment other public transportation methods for longer trips.
2.	Most trips start and end below Central Park. These trips average the shortest distances, most likely due to the increased density of public transportation options in comparison to outer neighborhoods and boroughs.
3.	Citi Bike strategies for distribution of bikes, i.e., “rebalancing”, must consider weather conditions for optimal bike and docking availability throughout the Citi Bike network.
4.	Holiday bike behavior differs; thus, Citi Bike must consider holidays when planning rebalancing.
5.	The pandemic had a significant impact on bike behavior.
6.	Exogenous factors, such as weather, often determine if a rider will use a bike, but once started, ride characteristics are relatively unchanged regardless of circumstances.

...

## Results and Conclusions
* There are regional differences in bike behavior in NYC that help contextualize city-wide cycling-as-transportation. Understanding regional and conditional variations in behavior can improve Citi Bike operations and inform strategies to increase bicycle use.
* Our dataset was insufficient for predicting trip start and end neighborhoods. Both the RF champion and Logistic Regression challenger models fail to predict inter-neighborhood rides accurately. However, most rides start and end in the same neighborhoods, so inter-neighborhood rides are anomalous - rides from Neighborhood A to B never represent more than about 6% of total rides in the full dataset for A ≠ B. Though we hoped these data could be used to predict start-to-finish commutes, our data were insufficient; we posit that most riders are biking intermediate point-to-point trips rather than directly to their destination. If the data tracked person behavior across all public transportation rather than bike behavior, the data would be better balanced and likely better for prediction.
* year is the most important feature for predicted distance. Each of the three contending models in our distance study identified the year 2020 as a significant predictor. Users travelled roughly 0.09 miles further in 2020. This was explained by the pandemic’s notable effect on transportation (i.e., a disinclination to ride public transportation during a pandemic would influence a user to bike a longer distance). user-type is also a notable feature in predicting distance. Subscribers travelled 0.07 miles less than one-time users of Citi Bike, and attraction-based stations have longer distance predictions (e.g., Central Park and The Bronx Zoo). Unsurprisingly, temperature has a positive impact on distance travelled.
* Station rank is affected by GOOD vs. BAD weather. Specifically, stations closer to the center of lower Manhattan are more important for station balancing during bad weather. Additionally, precip and feels_like are the most important variables affecting the count of bike trips by day. 
* Prior to down sampling, holidays represented only ~2% of the data, indicating possible overfitting issues and contributing to model difficulty due to lack of data. After down sampling, both the base and challenger model favor features relating to temperature, subscriber count, trips per day, distance traveled, and precipitation. Users travel less on holidays, and temperature is important for determining holidays. Understanding characteristics of holiday bike trips can help Citi Bike with bike rebalancing initiatives. 
* The predictiveness of the RF regressor model is high with a R^2 value of 0.876 and RMSE that was roughly ⅓ of the standard deviation of the average housing sales price. Warmer temperatures, subscriber count, sd. of crow-flies distance, and end-station statistics are the most important feature weights. The model is more accurate at lower sales prices. Citi Bike can use this analysis to determine where to place additional stations as they contain latent factors describing riders and their behaviors.

## Summary
We gained notable insights into user behavior through our analyses. While this can help Citi Bike’s decisioning, we recognize that further data collection (namely user-specific and intermediary-transport data) will offer high return when predicting user behavior. User-specific analysis will improve goodness-of-fit and complement insights gleaned from available data, particularly if Lyft can cross-sell car rides through the Lyft app with Citi Bike rides. With more data, we would begin with user-specific analysis to tie the whole project together.

