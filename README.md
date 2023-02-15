# Vacancy Days Analysis of Public Housing 

The objective of this data analytics project was to investigate the extent of public housing vacancies in QLD and the impact of COVID-19 on these vacancies. The project focused on the waiting list for permanent housing for victims of family violence, which has blown out to 17 to 24 months due to the high number of vacant apartments.

The project involved collecting and analyzing data from various sources, including government reports, housing agencies, and public records. The data was processed and analyzed using statistical techniques and visualized using charts and graphs to identify trends and patterns.

The results of the analysis showed that there were hundreds of public housing apartments that were vacant in QLD, despite the high demand for housing from victims of family violence. The data also revealed that the number of vacant apartments had decreased due to the impact of COVID-19, which had caused a decline in the number of people moving into public housing and results in a higher waiting period for the applicants.

The project provided valuable insights into the public housing crisis in QLD, highlighting the need for more effective strategies to address the growing demand for permanent housing. The findings of the project can be used by policymakers and housing agencies to develop more targeted and efficient solutions to the public housing crisis, thereby improving the quality of life for vulnerable communities.
<hr>
<br/>

# Datasets

The rental vacancy datasets were collected from data.gov.au in CSV format. There were five csv files and each file contains one financial years data. 

Source 1 https://data.gov.au/dataset/ds-qld-4e9daf44-8e3f-461d-b09c-f0247949ec9f/details?q=rental%20vacancy

Covid dataset was collected from Qld gov website.

Source 2 https://www.data.qld.gov.au/dataset/queensland-covid-19-case-line-list-location-source-of-infection

<hr>
<br/>

# Extract Transform and Load

An ipynb(etl.ipynb) file was created to preprocess the data and to store the clean data in one file(all_vacancy_data.csv).

<hr>
<br/>
	
# 	Data Analysis and Visualization

Yearly graph of average vacancy days showed upward trend till 2019 and then start falling. The anticipation the reason for this was the rise of covid-19 cases in the community.


<p align="center">
  <img src="Images\Avg VAC Days by Year.png" height="200"/>
  <img src="Images\pct_cng_year.png" height="200"/>
</p>  
<br/>
The Tenantable and the Untenantable part of the vacantdays were not much different throughout the years. However the average Tenantable vancant days were bit higher on 2018 and 2019.


<p align="center">
  <img src="Images\Untenable vs Tenable VAC Days.png", width='600'/>
  <img src="Images\ut_t_pie.png", width='600'/>
</p>  
<br/>

An abnormality in average vacant days distribution on number of bed rooms was observed.

<p align="center">
  <img src="Images\avg_vac_bed1.png", width='600'/>
  <img src="Images\Average Vacancy Days by Bedrooms and Rental Unit Type.png", width='600'/>
</p>  
<br/>

Dig deeper the reason of this abnormality box plot and qurtile analysis were done. And removed the outliers of Total Vacancy Days, Untenantable and Tenantable values.

<p align="center">
  <img src="Images\ttl_vac_box.png", width='200'/>
  <img src="Images\vu_box.png", width='200'/>
  <img src="Images\vt_box.png", width='200'/>
</p>  
<br/>

A rapid fall on vancancy count and total vancant days was observed in the time series analysis.

<p align="center">
  <img src="Images\Average Vac Days by Months.png", width='600'/>
  <img src="Images\poly_reg.png", width='600'/>
</p>  
<br/>

To explain the fall Covid-19 case number data was introduced.

<p align="center">
  <img src="Images\avg_vac_covid.png", width='600'/>
  <img src="Images\vc_count_covid.png", width='600'/>
</p>  
<br/>
<hr>
<br/>

# Usage
The datasets are stored in __"raw_data"__ directory. And the clean dataset after ETL is stored in __"Processed"__ Directory. And all the additional documents are in __"slides"__ directory.
