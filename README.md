# Cyclistic-bike-share-analysis-case-study
Bike renting company called "Cyclistic bike" , a data analysis performed on bike-share as case study 
----------> create new table and join 12 month data in this new table by using UNION function  <----------

CREATE table cycle (
SELECT * 
FROM divvy_tripdata2105 
UNION 
SELECT * 
FROM divvy_tripdata2106
UNION 
SELECT * 
FROM divvy_tripdata2107
UNION
SELECT*
FROM divvy_tripdata2108
UNION
SELECT*
FROM divvy_tripdata2109
UNION
SELECT*
FROM divvy_tripdata2110
UNION
SELECT*
FROM divvy_tripdata2111
UNION
SELECT*
FROM divvy_tripdata2112
UNION
SELECT*
FROM divvy_tripdata2201
UNION
SELECT*
FROM divvy_tripdata2202
UNION
SELECT*
FROM divvy_tripdata2203
UNION
SELECT*
FROM divvy_tripdata2204);
.
.

---------> find ride length by using start and ended (datetime) columns from table <----------

select
ride_id, rideable_type, start_lat, end_lat, start_lng, end_lng, member_casual,
time(ended_at - started_at) as ride_lenght
from cycle
.
.

----------> from cycle table , extract max , min and avg values to perform data alaysis <---------

SELECT * FROM CYCLISTICS.`cycle`;
select avg(ride_lenght) from `cycle`;
select max(ride_lenght)from `cycle`;
select min(ride_lenght)from `cycle`;
SELECT dayname(started_at), Dayofweek(started_at) from `cycle`;
.
.

--------->change data format from DateTime to Time by using Time() <---------

select
ride_id, rideable_type, start_lat, end_lat, start_lng, end_lng, member_casual,
time(ended_at - started_at) as ride_lenght
from cycle

UPDATE [table] SET [column]=0 WHERE [column] IS NULL¨ 

[Report Cyclistic.docx](https://github.com/ipriyapratapsingh/Cyclistic-bike-share-analysis-case-study/files/8587062/Report.Cyclistic.docx)

----------> got total 11 columns in final result <----------
