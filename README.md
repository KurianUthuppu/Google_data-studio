# Google data-studio
_Will take you through the basics of Google data-studio_

### Requirements
* Valid Google account
* Browser - Chrome / Firefox

### Resources
Google data-studio login - https://datastudio.google.com/
- Login via your Google account
- Google data studio comes free with google account
Helpful docs are available here -> https://support.google.com/datastudio#topic=9706750

### Loading data source with data via connectors
- Go to data sources tab and then click 'Create data source'
- Connect to requisite data via various connectors including google excel, analytics and big-query
- Alternatively, to export data from big-query, you can use the 'Export with Data-studio' option under export that is available when you click a particular data-table

### Creating Reports
- Once the data-source is connected via the requisite connector, one could see the various column headers under dimensions
- One can create additional dimensions/columns using 'Add a field' option; this could be calculated field based on the loaded dimension (more on this later)
- You may add a paramater if values have to be accepted from the customer which would reflect on the data-visualization dashboards
- You may set the data refreshness to 15 mins for faster response to edits on source data
- Once you are satisfied with dimensions and its types, you can create a report using 'Create report' option on the top-right corner

### Building dashboards
- You can easily create the requisite dashboards using various charts and inserting various controls
- The important part is to be clear on what exactly you are trying to value-add to the user in terms of extracting information/insights from data
- This will lead to how exactly the data visualization to be done, using which dashboards or controls
- Once the mental design is clear, it's about creating the dashboards which is sort of relatively easy
  - Thumb rule - Drag drop the requisite values for x axis in dimension, and the y axis values in metric
  - Use style the option to customize further
- You can create new fields or add new parameters (to accept real-time user inputs) as well
  - You can use simple formula to create calculated fields; example as below:
```
CASE
  WHEN FAT >= 5 THEN "Buffalo"
  ELSE "Cow"
END
```
- Final steps may require some trail & error as things may not have come exactly as you had envisioned
- You can view some of the dashboards that I had created to help analyze the IoT data of 
  - Daily milk procurment from a dairy to analyze trends 
  - The quantity/quality variations in farmer pouring which help to detect adulteration
  - Finding loan eligible farmers based on milk pouring trend (Attendance and Quantity) and calculating loan ticket size based on user inputs
  (Note: Some of the values are hidden due to confidentiality)

### Data-Studio - Pros/Cons
#### Pros
- Easy to learn and use
- Easy integration with different data sources including Big-Query which helps to store and give faster response for big data
  - Data with more than a 100K cells in excels gets too slow to load and reflect data; Big-Query is alternative for such big-data scenarios
- Free with google account
- Good documentation and youtube videos from Google
- Good ready made templates and options for customization

#### Cons
- Slow response to data edits in google excel sheets
- Sometimes few visualization bugs are visible during loading

PS: 
- Didn't allow embedding of google maps (Geo-chart dashboards) in google site  
  (Issue resolved on Oct-21: https://issuetracker.google.com/issues/155529836?pli=1)

