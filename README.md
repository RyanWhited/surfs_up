# Surfs_Up Challenge
![Surf Ice Cream](https://github.com/RyanWhited/surfs_up/blob/main/resources/surf_ice_cream.jpg)
## Overview
To help with the decision of an investor to launch an ice cream/surf shop in Oahu, HI, I analyzed preciptation and temperature data from multiple stations dating between the years 2010 - 2017. In this challenge, the investor specifically wanted the temperature data for the months of June and December in Oahu in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results
  1. Using the extract function from SQLAlchemy I was able to pull out the specified data for the months of June and December. 
  
    - June
      - june_results = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date)==6).all()
    - December
      - dec_results = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date)==12).all()
      
  2. Using the panadas describe function, here are the summary statistics for the June temperature DataFrame.
  ![Surf Ice Cream](https://github.com/RyanWhited/surfs_up/blob/main/resources/june_summary.png)
      
  3. Using the panadas describe function, here are the summary statistics for the December temperature DataFrame.
  ![Surf Ice Cream](https://github.com/RyanWhited/surfs_up/blob/main/resources/dec_summary.png)
      
## Summary
- Based on these results, the average temperature for both months is low to mid 70s. Not too hot so your ice cream won't melt in the sun in seconds and not too cold to enjoy this cold treat year round on the beach!
- The low temps in December can get into the 50s. It might be worth considering different operation hours to close up shop once the sun goes down as business might naturally slow down. 
- If we had the data available, I would suggest doing queries on wind speed and ground swells. After all, if we're selling ice cream AND surf supplies, you need some surf!
