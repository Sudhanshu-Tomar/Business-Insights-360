# Business-Insights-360 

![1_z8-MhqVp0wtdrnCVUWNKWw](https://user-images.githubusercontent.com/119277783/235495883-5675aba5-ceb8-4169-88f6-9addbb81388e.gif)

![business-analytics](https://user-images.githubusercontent.com/119277783/235479837-8904aa1b-1698-4182-9516-8ccc2afb164d.gif)




# Report 
 
 
 Click on the link below to view the report : 
 
 Power BI : https://app.powerbi.com/view?r=eyJrIjoiNWUwZTExYTMtMTYwOS00M2YzLWI2MmItOTk1YzU4ZjlmOTBhIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9
 
 NovyPro :  https://www.novypro.com/project/business-insights-360-8  
 
 
# Project Overview 

AtliQ Hardware is a company that supplies computer hardware and accessories to its customers. Despite being a rapidly expanding company in the electronics industry, it experienced substantial losses in Latin America due to a lack of data-based decisions. To tackle this issue, AtliQ Hardware has taken the initiative to hire a team of data analysts and utilize data insights to make well-informed decisions during its yearly strategic meeting. This decision was prompted by the success of their chief rival, Dell, which has already incorporated a data analytics team and employs data-driven decision-making to succeed in the market. 




# Tech stacks
  - SQL
  - PowerBi Desktop
  - Excel
  - DAX language
  - DAX studio (for optimizing the report)
  - Project charter file



# Power BI Techniques Learnt : 

As you continue to work with Power BI, you will discover various techniques that can help you create more effective and efficient reports. Here are some of the techniques that I have learned during this project 

  - Asking the right questions before starting the project
  - Creating calculated columns
  - Creating measures using DAX language
  - Data modeling
  - Using bookmarks to switch between two visuals
  - Page navigation with buttons
  - Using the divide function to prevent zero division errors
  - Creating a date table using M language
  - Dynamic titles based on the applied filters
  - Using KPI indicators
  - Conditional formatting the values in visuals using icons or background color
  - Data validation techniques
  - Power BI services
  - Publishing reports to Power BI services
  - Setting up personal gateway to set up the auto refresh of data
  - Power BI app creation
  - Collaboration, workspace, access permissions in Power BI services
  - And more.
  
  
#  Business related terms

  - Gross price
  - Pre-invoice deductions
  - Post-Invoice deductions
  - Net Invoice sale
  - Gross Margin
  - Net sales
  - Net profit
  - COGC - cost of goods sold
  - YTD - Year to Date
  - YTG - Year to Go
  - Direct
  - Retailer
  - Distributors
  - Consumer  


# Company’s back ground

AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel

  - Retailers
  - Direct
  - Distributors
  
  
Recently the company has faced a unforeseen loss by opening store in America based on the surveys, intuition and some excel analysis and also the company’s competitors has handful of analytics team to perform analysis and make data driven decision. So, the AltiQ hardware has no other option other than building their analytics team for data driven insights and decisions in the future to survive better in the industry.


Project kick off session, where you should get clear of for what and why this project and all other questions you have with regards to the project


# Questions to ask before starting with dashboard 


![thinking-hmm](https://user-images.githubusercontent.com/119277783/235492002-18221407-1f67-4468-a424-a5e775bad4ad.gif)

   
   - What is the objective of building this Power BI dashboard?
   - In what terms will the success of this project be measured?
   - What will be the deadline for the project?
   - Do the stakeholders expect a preview before the actual release?
   - What are all the hopes that stakeholders have for this project?
   - What are all the fears that stakeholders have in terms of building this dashboard?
   - Who will be using this dashboard, and for what purpose?
   - What are all the expectations that stakeholders have for the completion of this project?
   - What can go wrong while building this project?
   - What are all the resources and data needed to build this dashboard?
   - Is there any input from stakeholders in terms of the design and views of the dashboard?


After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.


# Dataset Understanding.


![74YE](https://user-images.githubusercontent.com/119277783/235492415-9ac87f85-a5a3-4883-a109-fcb18be6fd7d.gif)



   Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

  - Dimension table : It will have the static data like details of customer and products

  - Fact table : It will have the data about the transactions

  - gdb041:
     - dim_customer
          - 27 distinct markets (ex India, USA, spain)
          - 75 distinct customers thorough out the market
          - 
      - 2 types of platforms
          - Brick & Motors - Physical/offline store
          - E-commerce - Online Store (Amazon, flipkart)
      - Three channels
          - Retailer
          - Direct
          - Distributors
      - dim_market
          - 27 distinct markets (ex India, USA, spain)
          - 7 sub-zones
          - 4 regions
          - APAC
          - EU
          - nan
          - LATAM
      - dim_product
          - Divisions
          - P & A
          - Peripherals
          - Accessories
          - PC
          - Notebook
          - Desktop
          - N & S
          - Networking
          - Storage
       - There are 14 different categories, Like Internal HDD, keyboard.
       - There are different variants available for the same product.
       
      - fact_forecast_monthly
         - This table is used to forecast the customer’s need in advance, which can help in
         - Higher customer satisfaction
         - Reduced cost in warehouses for storage purpose
         - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
         - All the date of the month will be replaced by the start date of the month.
         - It will have all the column names and in the end it will have the forecast quantity need of the customer.
         
       - fact_sales_monthly
         - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.


  - gdb056
     - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
     - gross_price
        - Has the details of gross prices with product code
     - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
     - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
     - Post_invoice_deductions
     - Post invoice deductions and other deductions details



# Importing data into PowerBi

  - As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential . 
     
     
# Data Model
     - Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
     - Poor data modeling affects the over all performance of the report.
     - Following Good practices of data modeling is must. Refer this page to get to know the good practices Blog
     - In this project, we have followed Snowfall data modeling method.     
     
     

<img width="838" alt="Data_model" src="https://user-images.githubusercontent.com/119277783/235488963-9c418c10-b792-46fb-a153-0c55f3a71dd0.png">




# Dashboard designing
    - Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required

# Home view
    - In Home view, all the views button will be available. User will land on specific view page by clicking the button.

          - Info
          - Finance View
          - Sales View
          - Marketing View
          - Supply chain View
          - Executive View
          - Support
          
          
# Overall Report 




https://user-images.githubusercontent.com/119277783/235494846-9048e419-682a-4edd-bce1-f3f308a7f142.mp4





 Power BI : https://app.powerbi.com/view?r=eyJrIjoiNWUwZTExYTMtMTYwOS00M2YzLWI2MmItOTk1YzU4ZjlmOTBhIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9
 
 NovyPro :  https://www.novypro.com/project/business-insights-360-8  
 
 
 




# Project Outcome
    - The importance of data-driven decision-making in the business world.
    - The use of Power BI for creating effective and efficient reports.
    - Techniques for creating calculated columns, measures, and data modeling using DAX language.
    - The use of bookmarks and page navigation with buttons to switch between visuals.
    - Creating a date table using M language and dynamic titles based on applied filters.
    - KPI indicators and conditional formatting of visuals using icons or background color.
    - Data validation techniques and publishing reports to Power BI services.
    - Collaboration, workspace, access permissions, and setting up personal gateway for data refresh in Power BI services.
    - Business-related terms such as gross price, pre-invoice deductions, net sales, gross margin, net profit, cost of goods sold, etc.
    - The importance of asking the right questions before starting a project, measuring success, and understanding stakeholders' expectations and fears.
    - Understanding the available data through dimension and fact tables in the dataset.

  - These are some of the key learnings from the project.  





          

![animated-boy](https://user-images.githubusercontent.com/119277783/235491767-96ce052b-19de-432b-8a73-d91a37ab34de.gif)




  
  
