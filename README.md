# methane_emissions_estimation
Methane emissions estimates for Functional Urban Areas (FUAs) from Schiavina et al. (2019) provide information linking grid cells in the World Bank’s global XCH4 database to IDs for FUAs and national administrative units.

The database uses information from the European Space Agency’s Sentinel-5P (S-5P) (TROPOMI) satellite platform. It downloads monthly updates for georeferenced measures of XCH4—the column-averaged, dry-air mole fraction of the gas—and filters the data for atmospheric concentration anomalies that identify local emissions. The filter uses the methodology of Hakkarainen et al. (2019). See Dasgupta, Lall, and Wheeler (2023) for a detailed description.

#Summary
Here, we first merged the dataset for the years 2019-2022 and processed the merged output. We then checked for outliers and null values, but no issues were found, as the dataset was already in a standard format. The dataset was grouped for analysis in India since the dataset is global. Due to the large number of rows and for better analysis, sampling was done.

Next, seasonality and stationarity checks were performed through visual inspection and the Augmented Dickey-Fuller (ADF) test, which initially indicated non-stationarity. The series was then made stationary through differencing.

Afterward, our sampled dataset was ready for modeling, and ARIMA was applied. The forecasted values for the period between 1910-1950 (monthly mean bias-corrected XCH4) were quite close to the initial mean XCH4 values, indicating that there is not much increase or decrease if the conditions remain ideal.
