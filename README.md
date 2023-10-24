# What Drives LNG Spot Prices?

Welcome to my GitHub portfolio, where I showcase the job market paper of my dissertation, "What Drives LNG Spot Prices?" This project represents my efforts to replicate the findings from my dissertation using Python. In my dissertation, I analyzed the dynamics and volatility of LNG spot prices in Asian and European markets. While working on my dissertation, I utilized Eviews, a prominent econometric and forecasting software. Here, I reproduce my research findings using Python. 

![lngvessel](https://github.com/energyeconomist/LNG_price_dynamics/assets/11807759/dedc236a-9868-406d-a36e-600765d866ed)

## Table of Contents

- [Research Puzzle](#research-puzzle) 🧩
- [Data](#data) 📊
- [Methodology and Results](#methodology-and-results) 📈


### Research Puzzle 

In my dissertation, I examined the dynamics of LNG spot prices in Asian and European markets, focusing on the factors that drive these prices. LNG long-term contracts are already linked to oil and hub-based pricing, making it an intriguing question to determine what factors influence LNG spot prices. To address this question, I collected data on LNG and natural gas long-term contract prices, crude oil and coal prices, charter rates, heating and cooling degree days, and industrial production indices. I then analyzed their effects on LNG spot prices, using weekly time-series data spanning from the beginning of 2010 through the end of 2015 for the largest LNG market in the world (Japan), largest LNG trading hub in Europe (U.K.), and the world’s largest LNG re-exporting hub (Spain).

### Data 

To investigate my research question, I employed a non-experimental design with a weekly time-series dataset covering nearly six years. The unit of analysis is the price level, and I have 304 observations (weeks). Key data sources include:

- **NBP Price**: The front-month forward price of LNG delivered ex-ship (DES) to the NBP hub in the UK, which also represents the spot price for Northwestern European markets. In 2010, trading volume of the United Kingdom’s NBP hub was larger than the sum of entire Continental European hubs. 
- **Spain Spot Price**: Represents Southwest Europe and is calculated as the average of DES front-month and second-month ahead forward prices of LNG delivered to Spain.
- **German Border Price (GBP)**: Represents the contract price for Northwest Europe. It is an average of assessed forward curves of major long-term contracts to the German market and the average price paid for natural gas sent from Russia, the Netherlands, and Norway to Germany through pipelines.
- **Contract Price for Japan**: The forward curve of the average price of DES LNG imported to Japan under long-term contracts.
- **Gas Storage Europe (GSE)**: Weekly natural gas storage ratio data for NBP hub.
LNG spot and contract prices, charter rates, and NBP natural gas storage levels data are provided by ICIS.
- **EGHW**: Monthly ‘manufacturing, electricity, gas, heat supply, and water’ (EGHW) data in industrial production indices of Ministry of Economy, Trade and Industry of Japan and Eurostat.
- **Brent Crude Oil Price**: Weekly Brent crude oil price is calculated as the weekly average of Brent and is pulled from the Energy Information Administration (EIA).
- **Coal Price**: Weekly Qinhuangdao coal prices are used as the representative coal price for Asian markets and ARA (Antwerp-Rotterdam-Amsterdam) coal price stands for the coal price in Europe.  Acquired from S&P Global Platts, the leading energy information provider - my previous employer.
- **Degree Days Data**: Cooling and heating degree days data are collected from wunderground.com, a partner company of The Weather Channel.

To ensure the completeness of the dataset, linear interpolation was applied to address missing values in some data series.

### Methodology and Results 

In this paper, I employed an Error Correction Model (ECM) to explore the dynamics that drive LNG spot prices in world markets. Prior to building the ECM, I conducted structural break, unit root, and cointegration tests to determine the existence of stable long-run relationships between the variables. I also ran causality tests to understand the direction of causality between the series.

If the time series are both integrated of the same order and cointegrated, then one can define an error correction model where the changes in the dependent variable is described by the changes both in independent variables and the dependent variable as well as an error correction term. Error correction term, α, shows the deviations from the long-run cointegration relationship for the cointegrated variables and the absolute value of α indicates how fast equilibrium is restored after that deviation. 

In my error correction model, I established causality from LNG contract prices to LNG spot prices if the coefficients of the error correction term and contract price were jointly significant. In such kind of case, a shock that drives the spot price out of its long-term relationship with contract prices can be corrected at a weekly rate of α, meaning that the spot price adjusts α% weekly to return to its long-run relationship with contract prices. 

My test results revealed that LNG spot prices in Japan and Spain were primarily driven by the NBP spot prices and the NBP spot prices were driven by crude oil prices. My results suggested that oil and (liquefied) natural gas prices have not decoupled and oil prices continued to drive LNG spot prices in spite of improving deregulation in Europe. Finally, even though coal is seen as a substitute for the natural gas in electricity generation, I found no cointegration between LNG spot and coal prices in any market due to mainly declining coal demand.

---

Thank you for visiting my GitHub portfolio and exploring my research on LNG spot prices. If you have any questions or would like to discuss this project further, please feel free to reach out to me.
