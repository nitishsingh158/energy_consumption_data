# Smart Meter kWh Readings

## Overview:
<p> Analyse and visualize kWh usage data for different demographic groups and different tariffs. Dataset consists of 5,566 London households and their half hourly kWh meter readings between November, 2012 and February, 2014.
Households have been categorized based on CACI ACORN(Classification of Residential Neighborhoods), which is a geo-demographic segmentation of UK's population. There are 6 such categories. Each of these 6 categories are further divided into groups, making a total of 17 groups. More information about ACORN groups can be found <a href="https://acorn.caci.co.uk/what-is-acorn">here</a>.</p>
	
<p>Energy tariff plans are categorized into two groups: Dynamic Time of Use and Standard. The Dynamic Time of Use plan is set up in such a way that each household is informed in advance of the specific times when their electricity tariff would be higher or lower than normal price – High, Low or normal. The Standard plan has a constant flat rate throughout the day. </p>

<p> <b>Note:</b> The dataset consists for 111 csv files each contaning data for about ~50 households based on thier geographical block. This analysis can be prompted to randomly select a sample of the dataset (default is ~8.5 million data points) to get sample statistics and observe any patters. 

--- 

### Summary of Analysis:

1. **Tariff Breakdown:** 

    The distribution of tariff based on three types of households: Affluent, Comfortable and Adversity and also on Time and Season
    - Affluent and Comfortable households have higher proportions of opt-ins for ToU rates, possibly because they can afford to pay the higher rates that are charged at peak hours.

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/tariff_breakdown.png" width="550" style="display: block; margin: 0 auto;">

    &nbsp;
    - The rate for ToU are high at peak times when the demand of energy is highest. Peak times occuraround mid-day in summers and morning and night in winters.

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/rate_breakdown.png" width="550" style="display: block; margin: 0 auto;">


&nbsp;

2. **Daily and Seasonal Consumption Patterns:** 

    General seasonal and monthly trends of energy usage.
    - Affluent and Comfortable households have higher cumulative energy usage in any month of the year.

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/median_monthly_usage_avg.png"  width="550" style="display: block; margin: 0 auto;">

    &nbsp;
    - From this dataset, it does not look like ToU is very effective in curtailing energy usage of consumers. Both in summer and winter the ToU households use more energy than Std tariff households. This is possibly because more Affluent and Comfortable households opt in for ToU and they anyways have high energy consumption.
    **note:** If we plot each group seperately, we get to see the variations within each group showing that the above is not true, and there are some ToU users in ACORN Q, H, L that have much higher consumptions thatn other groups. 

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/median_usage_time_of_day.png" width="550" style="display: block; margin: 0 auto;">

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/usage_by_groups.png" width="550" style="display: block; margin: 0 auto;">

    &nbsp;
    - From this dataset, we also see that ToU users have much higher monthly bills.

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/monthly_bill.png" width="550" style="display: block; margin: 0 auto;">


&nbsp;

3. **Peak Load Analysis:** 

    Determine the peak electricity load periods, which can help utilities prepare for high-demand periods and avoid overloading the grid.
    - Winter seems to have the highest demand for energy during the year, with the peak demand happening around 6:00 PM, just as people get home from work. Summer follows a similar trend but with lower energy usage. This means that utility has to solve for this peak energy demand when designing any energy intervention projects. 

    &nbsp;
    <img src="https://github.com/nitishsingh158/energy_consumption_data/blob/main/Images/load_profile_seasonal.png"  width="550" style="display: block; margin: 0 auto;">



&nbsp;
### **What else can we do with this data?**
The Acorn data is very comprehensive when it comes to breakdown by demographics. It has income, race, age, location among many other categories to create consumer segments. So the above analysis can b edone based on entirely different segments to compare ther enrgy usage habit. 

- **Load Profiling:**
   - Create load profiles for different customer segments (e.g., residential, commercial, industrial) to tailor energy management strategies.
- **Demand Forecasting:**
   - Use historical data to forecast future electricity demand, helping utilities plan for capacity expansion or reduction.
- **Customer Behavior Analysis:**
   - Understand how different customer groups use electricity and develop targeted strategies to encourage conservation or reduce waste.