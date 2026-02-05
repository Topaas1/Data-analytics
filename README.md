# Power BI Project: Digital vs In-Person Healthcare Appointments

## Project Overview
This project analyzes core operational metrics of social and healthcare services in the capital area using fictional data. The goal is to compare two major cities—**Metro North (Metro Pohjoinen) and Metro West (Metro Länsi)**—and evaluate how effectively they are meeting their targets for digital (remote) healthcare appointments.

The analysis focuses on metrics such as:
- Ratio of remote vs in-person appointments  
- Appointments per employee  
- Total appointments by city  

This project was built using Power BI and is intended to demonstrate my end-to-end analytics workflow, from defining a business question to modeling data and presenting insights through visuals.

## Business Question
Healthcare home services aim to increase the share of digital appointments to reduce employee travel time and improve efficiency. A target has been set for at least **20% of appointments to be conducted remotely**.

The core questions addressed in this analysis are:
- How has **Metro North** performed overall in meeting this target?
- How does **Metro North** compare to **Metro West**, which introduced a similar target one year earlier?
- What operational differences might help explain the results?

## Data
The dataset used in this project is **entirely fictional** and was created to resemble a real-world transactional healthcare dataset. No real individuals, organizations, or locations are represented, and no privacy or copyright concerns apply.

## Methodology
1. Defined a realistic business question based on a familiar healthcare context.
2. Created a fictional transactional dataset representing healthcare appointments.
3. Imported the data into Power BI and cleaned it using Power Query (e.g. handling missing values).
4. Normalized the data into a star schema, separating fact and dimension tables.
5. Built a data model with relationships between time, area, and fact tables.
6. Created key measures, such as:
   - Ratio of remote to in-person appointments  
   - Appointments per employee
7. Designed interactive visuals, including bar charts, cards, and slicers to compare cities.

## Example DAX Measures
Below is an example of a key metric used in the analysis to calculate the share of remote appointments:



```DAX
Etä_Osuus_% =
DIVIDE(
    SUM(Fakta_Palvelut[Joista etäkäyntejä]),
    [Käynnit yhteensä]
) * 100
```

## Key Findings
- The share of remote appointments in **Metro North** is significantly lower than in **Metro West**.
- **Metro North** shows a higher number of appointments per employee, suggesting differences in available resources.
- Despite higher efficiency per employee, the gap in digital appointment usage remains substantial.

## Conclusions and Next Steps
The results indicate that **Metro North** may benefit from further investigation into barriers to digital healthcare adoption. Possible next steps include:
- Assessing digital literacy among employees and customers
- Evaluating access to and usability of digital devices
- Exploring organizational or cultural factors affecting adoption

This analysis highlights how data can support operational decision-making in healthcare services.
