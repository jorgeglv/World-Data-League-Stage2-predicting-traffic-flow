# World-Data-League-Stage2-predicting-traffic-flow

**Context**

According to the European Environment Agency, passenger cars are a significant polluter,
accounting for 60.7% of total CO2 emissions from road transport in Europe. Without a
doubt, congested cities are a significant contributor to this.
The city of Porto has been counting cars at several locations with Inductive Loop sensors
since 2015. With this historical data, it should be possible to predict the traffic flow and
especially intense periods of traffic.
By predicting the traffic flow in the city and understanding the factors that influence the
traffic, it’s possible to take action into reducing the traffic.

**Goals**

On the one hand, the goal of this challenge is to create an explainable prediction of when
heavy flow and congestions in the city will happen. On the other hand, it shows that it is
possible to extract useful insight regarding the traffic by using sensors in several locations.
By achieving this, it is possible to create tools for the city to manage the traffic much
better by achieving this, thus reducing the CO2 emissions.

**Outcome**

The outcome of this challenge is three-fold:

● Create a predictive model for traffic flow in the city of Porto for different periods
of the day from sensor data;

● Explain which factors affect the traffic flow;

● Show any relationship and insights that exist between the different traffic flow in
the city.

For this challenge, you must use sensor data from induction loops, but you can also use
other data.

**Solution**

First, we have built a generic SEASONAL ARIMA model to predict traffic flow in the city. As the traffic varies greatly depending on location, we have grouped streets according to flow similarity into three clusters. On top of that, we have fit a SARIMA model for each cluster to better represent and forecast traffic flow.

As for the second and third objectives, we have done an exhaustive analysis of variables that may affect traffic intensity, not only those provided in the challenge like weather conditions and POI's, but we have included COVID incidence. This is better described in the section "Assessing dimensions impacting traffic-flow," but we have reached the conclusion that the main factor that affects traffic intensity in the POI's, followed by weather conditions.

COVID doesn't seem to affect traffic, but this is because the timeframe corresponds to 2021 between January and April while Portugal has been locked down. For this reason, changes in COVID incidence don't affect traffic flow as it has already influenced the overall situation.

With all this information, we can predict traffic peak hours and its relationship with POIs, weather, and COVID.
Some measures can be implemented to reduce traffic. For example, to increase public transportation services at hours where intensity is higher, thus reducing intensity and also reducing carbon footprint in general.
