# Citi Bike Usage in New York City
## Big Data Systems (DS 5110)
August 11, 2021
Diana McSpadden (hdm5s)

Nick Daniello (njd9e)

David Fuentes (dmf4ns)

Eric Sarani (es5cj)

Abigail Bernhardt (aeb4rv)

## REPO CONTENTS
* Code_HTML: html version of ipynb files
* Code_IPYNB: python notebooks
* EDA_Images: EDA plots required for course final project
* Figures: Figures included in final report
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

