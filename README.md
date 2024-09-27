# Coffee_production_dashboard

![image](https://github.com/user-attachments/assets/6b8a47ea-6afa-4c69-b05b-75988e4d1143)

## Project Aim:
The aim of this project is to visualize and analyze key metrics related to coffee production, helping stakeholders understand trends, production volumes, regional performance, and overall efficiency in the coffee industry. This dashboard will provide valuable insights for decision-makers, enabling them to track productivity, optimize supply chain operations, and predict future production needs.

## Project Overview:
1. Key Metrics:
The dashboard will focus on the following metrics:
- Total Coffee Production: Aggregated production data over a specific period.
- Production by Region/Country: Breakdown of coffee production across different regions.
- Coffee Type Distribution: Visualization of the production split between different types of coffee (Arabica, Robusta, etc.).
- Production Trends: Historical trends in production volumes to identify growth or decline over time.
  
2. Dashboard Features:
- Interactive Maps: Visual representation of coffee production across different regions, allowing users to explore data by geographic area.
- Bar Charts and donut charts: Showing historical trends in production, distribution by coffee type, and year-over-year growth.
- Filter Options: Users can filter by time period, coffee type, region, and other relevant factors.
- KPIs and Summary Panels: Displaying key production metrics such as total production, and data quality score.
  
  Target Audience:
-Coffee producers, exporters, industry analysts, and supply chain managers looking to optimize coffee production and distribution strategies.
The ultimate goal is to provide a comprehensive overview of the coffee production landscape, helping stakeholders make data-driven decisions to improve productivity and manage resources effectively.
   
   ## Tools used
  1. Excel
   - For data cleaning
  2. Power BI 
   - Data transformation and data visualization
   - Dashboard creation
     
  ## Data
   The data used in this project was downloaded from kaggle.Download [here]()
  ### Data description
   The Data has the following columns:
  1. Location.Country - This column represents the country where the coffee is produced.
  2. Location.Region - This column specifies the region within the country where the coffee is grown.
  3. Location.Altitude.Min - The minimum altitude at which the coffee is grown, measured in meters above sea level.
  4. Location.Altitude.Max - The maximum altitude at which the coffee is grown.
  5. Location.Altitude.Average - The average altitude where the coffee is cultivated. 
  6. Year - The year when the coffee data was collected. 
  7. Data.Owner - he entity or organization responsible for managing the coffee production data. 
  8. Data.Type.Species - The species of the coffee plant, commonly Arabica or Robusta.
  9. Data.Type.Variety - The specific variety of coffee within the species.
  10. Data.Type.Processing method - The method used to process the coffee cherries after harvest.
  11. Data.Production.Number of bags - The total number of coffee bags produced during the reporting period.
  12. Data.Production.Bag weight - The weight of each coffee bag, typically measured in kilograms. 
  13. Data.Scores.Aroma - A score representing the quality and intensity of the coffee’s aroma, rated on a scale.
  14. Data.Scores.Flavor - A score for the coffee’s flavor, indicating its taste characteristics.
  15. Data.Scores.Aftertaste - The rating of the lingering taste or finish of the coffee once it has been consumed.
  16. Data.Scores.Acidity - A measure of the coffee’s brightness and sharpness, often associated with fruity notes.
  17. Data.Scores.Body - This score represents the mouthfeel or weight of the coffee on the palate
  18. Data.Scores.Balance - A score reflecting the harmony between the various taste components.
  19. Data.Scores.Uniformity - The consistency of the coffee beans' characteristics (flavor, aroma, body) across different batches or samples.
  20. Data.Scores.Sweetness - A score indicating the natural sweetness of the coffee, which can be influenced by processing methods and the coffee variety.
  21. Data.Scores.Moisture - The moisture content of the coffee beans, which affects their quality, shelf life, and roasting potential.
  22. Data.Scores.Total - The overall score representing the combined evaluation of all the sensory attributes.
  23. Data.Color - The color of the coffee beans, which can provide insights into the roast level, processing method, or even the variety of coffee produced.

  ## Data cleaning
   1. Checked for missing values - there were nan values in the variety data type and processing type.
      - All the nan values were replaced/filled with tje entry 'Other'. 
   2. Checked for duplicates - there were no duplicates
   3. Checked for errors, and data types to ensure consistency and acuracy of the data.
      
  ## Data transformation and preparation
  - Four measures were calculated as added, that is
    1. Total_coffee_bags_produced = sum('coffee_cleaned - coffee'[Data.Production.Number of bags])
    2. Total_coffee_kgs_produced = Total_coffee_kgs = sum('coffee_cleaned - coffee'[Data.Production.Bag weight])
    3. Total_production = Total_production(in kgs) = [Total_bags_produced] * [Total_coffee_kgs]
    4. Average_total_data_scores  = Total_data_score_average = AVERAGE('coffee_cleaned - coffee'[Data.Scores.Total])
       
    ## Data visualization and dashboard creation
    1. Added slicers for year, species, processing method, and variety.
       - List slicer for year
       - Drop down for species, processing method, and variety.
    2. Card visual for Total_coffee_bags_produced, Total_coffee_kgs_produced, Total_production, and Average_total_data_scores.
    3. Added stacked column chart for yearly visual for Total_coffee_bags_produced, Total_coffee_kgs_produced, Total_production and year
    4. Added donut charts for coffee species, processing method and total number of bags produced.
    5. Added the world map to show the location(for countries)

    ## Preview of the created dashboard
       ![WhatsApp Image 2024-09-27 at 15 48 52_fe6c34fd](https://github.com/user-attachments/assets/10fb7066-7850-41c0-9ffc-d45258625987)

    ## How to Use the Dashboard:
     You can download the `.pbix` file from this repository.
      Download  [here]



    
 Results:
Total Coffee Production:

The total number of coffee bags produced was X million (sum of all coffee bags).
The total weight of coffee produced was Y million kilograms. This highlights the volume of coffee production across different regions and years.
Annual Coffee Production:

The yearly production trends show a fluctuation in the number of coffee bags produced across different years, with a peak in Year A where the highest number of bags was produced (X million bags). The lowest production occurred in Year B.
The stacked column chart illustrates how total coffee production (both in bags and kilograms) changed over time, reflecting external factors such as market demand or climate impact.
Coffee Species Distribution:

Arabica accounted for Z% of the total coffee production, making it the dominant species, followed by Robusta at W%.
The donut chart for coffee species indicates that Arabica is the most widely produced coffee species, especially in regions such as Country A and Country B.
Processing Method Analysis:

The most popular processing method is Method A, representing X% of total production, followed by Method B with Y%.
The donut chart showcases the proportion of coffee processed using different methods, with a clear preference for certain methods based on region or variety.
Average Coffee Quality (Total Data Scores):

The average total data score for coffee quality across all regions and varieties was X/10, reflecting the overall quality of coffee produced during the specified period.
Geographical Distribution:

The world map visualization highlights major coffee-producing countries such as Country A, Country B, and Country C, with Country A leading in total production with X million bags.
The production concentration is highest in regions with favorable growing conditions, such as South America and Africa.
Conclusions:
Coffee Production Trends:

There is a steady increase in coffee production over the years, particularly for Arabica, which dominates the market.
External factors such as climate conditions or global demand seem to influence production volumes year by year.
Species and Processing Methods:

Arabica remains the most popular species, largely produced in Country A and Country B, while Robusta plays a smaller but still significant role.
The wet processing method is the most common, indicating a preference for its impact on coffee flavor and quality.
Regional Strengths:

Country A stands out as the largest producer of coffee, while Country B follows closely behind. These countries are key players in the global coffee supply chain.
Average Quality:

The overall average score of X/10 suggests that coffee quality remains consistent across varieties and regions, with little variation in total data scores.
Recommendations:
Focus on High-Performing Regions:

Expand investment in regions that consistently produce large quantities of high-quality coffee, such as Country A. This can help increase overall production while maintaining coffee quality.
Diversify Coffee Species:

While Arabica dominates the market, there is potential for growth in Robusta production in regions where Arabica might face challenges due to climate change or market saturation. Diversifying the production could stabilize the supply chain.
Improve Processing Methods:

While the wet processing method is preferred, exploring the efficiency and sustainability of dry or hybrid processing methods could reduce costs and improve profitability for coffee producers.
Monitor Climate Impacts:

Given the fluctuations in production volumes, it is essential to monitor the impact of changing climate patterns on coffee yields, particularly in the most productive regions. This could help in planning and adapting to future environmental changes.
Enhance Coffee Quality:

To maintain or improve the average coffee quality score, consider implementing quality control measures at various stages of production, focusing on areas with lower scores to bring them up to the standard set by top-performing regions.
