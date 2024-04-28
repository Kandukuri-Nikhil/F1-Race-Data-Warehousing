
# Formula 1 Race - Data Warehousing

## Problem Setting:
Formula 1, the pinnacle of motorsport, is a realm where speed, precision, and innovation
converge. With a storied history dating back decades, it captivates a global audience,
transforming drivers into legends and teams into engineering powerhouses. Yet, beneath the
excitement of roaring engines lies a colossal data challenge. Each race generates a torrent of
data, from car telemetry and driver performance metrics to real-time weather conditions and
fan interactions across digital platforms. Managing this data influx effectively is the linchpin for
revolutionizing Formula 1.

## Problem Definition
The problem at hand revolves around the Formula 1 ecosystem, where an escalating influx of
diverse data from sources like race telemetry, car sensors, driver metrics, weather conditions,
and fan interactions presents a pressing challenge. This challenge entails designing a
comprehensive solution for efficient data collection, processing, and real-time analysis. The
overarching goal is to leverage this wealth of information to optimize race strategies, enhance
vehicle development, and enrich fan engagement. Moreover, the project faces the formidable
task of managing high-speed data streams during races, while simultaneously prioritizing data
security and privacy. In summary, the problem definition centers on orchestrating effective
data management in Formula 1 to usher in a data-driven era that revolutionizes the sport's
performance and fan experience.
## Data Source:
The database consists of 14 tables and consists of all information on the Formula 1 races,
drivers, constructors, qualifying, circuits, lap times, pit stops, championships from 1950 till the
latest 2023 season. 

https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020/data


## Operational Business Context
1. **Enhanced Decision-Making**: The data warehousing project empowers Formula 1 teams with the data they need to make informed decisions regarding race strategy, car development, and driver choices. This can lead to improved team performance on the
track.

2. **Improved Fan Engagement**: For Formula 1 enthusiasts and fans, the project enhances the viewing experience by providing real-time updates, interactive content, and statistics that help fans better understand and enjoy the sport.

3. **Data-Driven Sponsorship**: Sponsors and advertisers can use the platform to evaluate the impact of their investments in Formula 1, allowing them to make data-driven decisions about future sponsorship opportunities.

4. **Regulatory Oversight**: Regulatory bodies can use the data warehousing solution to ensure that F1 races adhere to safety regulations and sporting rules, contributing to the integrity and safety of the sport.

5. **Historical Analysis**: All stakeholders benefit from access to historical data, enabling them to analyze trends, assess the evolution of the sport, and make predictions based on historical performance

In summary, the operational business context for the F1 data warehousing project revolves around providing valuable data-driven insights to a wide range of stakeholders, ultimately
enhancing the competitiveness, entertainment, and safety of Formula 1 racing while meeting the needs of teams, sponsors, media, and fans.







## Data Description
This dataset comprises a total of 9456 instances joined from multiple datasets such as Diet data, Lab data, Demographic data. There are a total of 27 attributes some of which are Age, BMI, Systolic Blood Pressure, Total Cholesterol, Glycohemoglobin and 1 target attribute - ‘Diabetes’.


##  Entity Relation Diagram (ERD)
![Image](https://github.com/Kandukuri-Nikhil/F1-Race-Data-Warehousing/blob/main/img/f1_eer.png?raw=True)

## Relational Schema
**Disclaimer**: There are too many attributes to entities, couldn’t fit everything in er-diagram so mentioning all attributes in relational schema.

**Primary keys** are in **Bold**
**Foreign keys** are in _Italic_

### Tables

- Driver(**driverId**,driverRef,number,code,forename,surname,dob,nationality,url)

- constructors(**constructorId**,constructorRef,name,nationality,url)
- Circuits (**circuitId**,circuitRef,name,location,country,lat,lng,alt,url)
- Seasons(**Year**, URL)
- Races(**raceId**, _circuitId_, year, round, name,date,time,url)
- Qualifying(**qualifyId**, _raceId_, _driverId_, _constructorId_,number,position,q1,q2,q3)
- Status(**statusId**, Status)
- Results(**resultId**, _raceId_, _driverId_, _constructorId_, number, grid, position, positionText, positionOrder, points, laps, time, milliseconds, fastestLap, rank, fastestLapTime, fastestLapSpeed, statusId)
- pitStops(_raceId_, _driverId_, stop, lap, time, duration, milliseconds)
- lapTime(_raceId_, _driverId_, lap, position, time, milliseconds)
- Target (**targetId**, _raceId_, _driverId_, win)
- driverStandings (**driverStandingsId**, _raceId_, _driverId_, points, position, positionText, wins)
- constructorStandings(**constructorStandingsId**, _raceId_,   _constructorId_, points, position, positionText, wins)
- ConstructorResults (**constructorResultsId**, _raceId_, _constructorId_, points, status)

## Conceptual Model:
![Image](https://github.com/Kandukuri-Nikhil/F1-Race-Data-Warehousing/blob/main/img/conceptual-f1.png?raw=True)

## Logical Model:

![Image](https://github.com/Kandukuri-Nikhil/F1-Race-Data-Warehousing/blob/main/img/Logical_Model_F1.png?raw=True)

**Developed an F1 data warehouse dashboard, leveraging insights from Formula 1 data to enhance decision-making and strategy formulation within the racing industry**

**BI Dashboard**
![Image](https://github.com/Kandukuri-Nikhil/F1-Race-Data-Warehousing/blob/main/img/F1_dashboard.png?raw=True)

**KPI’s and Metrics**:

From constructors' longevity and financial success to drivers' career duration and podium achievements, these metrics provide a holistic view of the sport's competitive dynamics. Our
exploration lays the foundation for informed decision-making and strategic planning, offering stakeholders a nuanced understanding of Formula 1's evolving landscape.

**Constructors**:

**_Duration of Constructor Participation_**:
Showcase the number of years each constructor has been actively involved in Formula 1 racing.

**_Constructor Winnings Analysis_**:
Illustrate the financial success of each constructor by highlighting their winnings over the years.

**_Total Podium Achievements by Constructors_**:
Explore the overall podium performance of each constructor through a comprehensive display of their total podium finishes.

**_Overview of Constructor Rankings_**:
Provide an insightful breakdown of the distribution of rankings among various constructors.

**Drivers**:

**_Career Duration of Drivers_**:
Highlight the number of years each driver has been actively participating in Formula 1 racing.

**_Winning Achievements by Drivers_**:
Showcase the success of individual drivers by presenting their winnings over the course of their
careers.

**_Total Podium Finishes by Drivers_**:
Explore the podium performance of drivers by illustrating the total number of times they haver eached the podium.

**_Accumulated Points by Drivers_**:
Evaluate the overall performance of drivers by displaying the total points they have earned throughout their careers.

**Conclusion**:

In summary, our report thoroughly examines the rank distribution among constructors and key performance indicators for drivers in Formula 1. The analysis offers insights into the competitive
landscape, diversity in rankings, and trends over time for constructors. For drivers, it highlights career duration, winning achievements, podium finishes, and accumulated points. These findings provide valuable information for stakeholders, teams, and enthusiasts, fostering informed decision-making and strategic planning in the dynamic world of Formula 1.
