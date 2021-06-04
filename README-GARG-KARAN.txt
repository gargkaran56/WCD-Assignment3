Introduction

Covid-19 had a significant impact on the fiscal, home and work experiences of Melbourne residents during 2020. To understand the impact of changes in 2020, researchers conducted a survey of 1000 Melbourne residents to explore the difference between their 2019 and 2020 experience with regards to mental health, financial stability and home life.

The survey was collected online through a survey platform called Qualtrics in the month of January, 2021. Respondents were invited to participate through a mailed invitation, from where they were encouraged to scan a QR code and complete the survey. Respondents first gave informed consent for the collection and use of their data, and the eventual distribution of de-identified data. At the conclusion of the survey, respondents gave an email address to which a Coles giftcard worth $20 was sent in compensation for their time.

This survey is a hypothetical example of data that might have been collected during this period. It does not have ethics approval, nor was it actually sent to participants. The data you have been given is simulated for teaching purposes and is not intended for analysis or interpretation.


A few helpful hints:

*  Weights have not been created for the data, so it will be analyzed without
*  Duration is the time spent doing the survey, and is measured in seconds
*  Missingness is stored in the usual R way as an NA. It comes from two sources. Firstly not all   participants completed the survey. Secondly, not all participants answer all questions. Notably most  who do not work in a given year do not answer work related questions.

Files included in this project:

1. release-data-Garg-Karan.csv (data folder) (open data ready for analysis)
2. data-dictionary-GARG-KARAN.Rmd.csv (data folder) (Data codebook containing info on all the variables used in open data)
3. GARG-KARAN.html (Analysis folder) (Report on making a raw_data into open data)
4. GARG-KARAN.Rmd (Analysis folder) (Code used to report on making a raw_data into open data)
5. header.html (Analysis folder) (Monash University header image html code, used in YAML section of code)
6. header.png (Analysis folder)  (Monash University header image)
7. monashreport.css (Analysis folder) (Monash University header image css/styling code, used in YAML section of code)
8. packages.bib  (Analysis folder)  (Bibliotex file containing all the citations to website/software/data used in making the report) 



Example Calculation:

What is the Avg. household income in 2019 and 2029 w.r.t age_groups?

data2 %>% 
  group_by(age_group) %>% 
  summarise(avg_inc_2019 = mean(new_house_inc_2019,na.rm = TRUE),
            avg_inc_2020 = mean(new_house_inc_2020,na.rm = TRUE))



