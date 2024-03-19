# Data-Science-Ensembling-Techniques-Project-EasyVisaProject-

**Context:**

Business communities in the United States are facing high demand for human resources, but one of the constant challenges is identifying and attracting the right talent, which is perhaps the most important element in remaining competitive. Companies in the United States look for hard-working, talented, and qualified individuals both locally as well as abroad.

The Immigration and Nationality Act (INA) of the US permits foreign workers to come to the United States to work on either a temporary or permanent basis. The act also protects US workers against adverse impacts on their wages or working conditions by ensuring US employers' compliance with statutory requirements when they hire foreign workers to fill workforce shortages. The immigration programs are administered by the Office of Foreign Labor Certification (OFLC).

OFLC processes job certification applications for employers seeking to bring foreign workers into the United States and grants certifications in those cases where employers can demonstrate that there are not sufficient US workers available to perform the work at wages that meet or exceed the wage paid for the occupation in the area of intended employment.

**Objective:**

In FY 2016, the OFLC processed 775,979 employer applications for 1,699,957 positions for temporary and permanent labor certifications. This was a nine percent increase in the overall number of processed applications from the previous year. The process of reviewing every case is becoming a tedious task as the number of applicants is increasing every year.

The increasing number of applicants every year calls for a Machine Learning based solution that can help in shortlisting the candidates having higher chances of VISA approval. OFLC has hired your firm EasyVisa for data-driven solutions. You as a data scientist have to analyze the data provided and, with the help of a classification model:

Facilitate the process of visa approvals.
Recommend a suitable profile for the applicants for whom the visa should be certified or denied based on the drivers that significantly influence the case status.

**Data Description**

The data contains the different attributes of the employee and the employer. The detailed data dictionary is given below.

case_id: ID of each visa application

continent: Information of continent the employee

education_of_employee: Information of education of the employee

has_job_experience: Does the employee has any job experience? Y= Yes; N = No

requires_job_training: Does the employee require any job training? Y = Yes; N = No

no_of_employees: Number of employees in the employer's company

yr_of_estab: Year in which the employer's company was established

region_of_employment: Information of foreign worker's intended region of employment in the US.

prevailing_wage: Average wage paid to similarly employed workers in a specific occupation in the area of intended employment. The purpose of the prevailing wage is to ensure that the foreign worker is not underpaid compared to other workers offering the same or similar service in the same area of employment.

unit_of_wage: Unit of prevailing wage. Values include Hourly, Weekly, Monthly, and Yearly.

full_time_position: Is the position of work full-time? Y = Full Time Position; N = Part Time Position

case_status: Flag indicating if the Visa was certified or denied

**EDA Summary of Observations**

There are some employers having huge employee base of more than 100000 employees spanning upto 602069 employees.

The Asian continent has highest number of 66% of applicants for US visa followed by Europe and North America.

40% of the candidates applying for USA work visa have completed Bachelor's degree. 37.8% of the candidates apllying for USA work visa have completed Master's degree.

58% of the candidates applying for USA work visa have prior job experience while 42% of the candidates doesn't have job experience.

The education of the employee has lot of value in determining the certification of the visa application.

Applicants with prior job experience has a probability of 70% of visa getting certified compared to applicants without job experience making only a 50% chance of visa getting certified.

The applicants from Europe has highest of 80% of Visa certification whereas the applicants from South America has the lowest probability of 58% of visa getting certified among all the other continents.

There are more than 2900 applicants who completed Bachelor's have selected their intended region of employment as either south or West.

Candidates applying to work for the employers who pay an yearly salary have less probability of their visa getting denied meaning the probability of the visa getting certified is 70% which is higher than other unit of wage.

Employers who pay Hourly salary have the visa certified rate to be very low close to 35% compared to all the other unit of wages such as Month, Yer and Week.

The median value of prevailing wage for cases of both certified and denied is close to 70000 dollars. However the median prevailing wage of cases certified is slightly higher than cases which are denied. Less than 25% of cases which are certified have prevailing wage of atleast 30000 dollars

**Actionable Insights and Recommendations**

The hyperparameter tuned XGBoost classifier model can be implemented to facilitate OFLC in determining the decision for visa certification process.

The features such as education of employees, previous job experience and the demography the employee applies from and the unit of wage plays a key role in determining whether the visa application should be certified or denied.

Candidates applying to work for the employers who pay an yearly salary have less probability of their visa getting denied meaning the probability of the visa getting certified is 70% which is higher than other unit of wage.Hence the OFLC can consider the unit of wage as a key factor for visa applications.

The job experience factor can be taken as a first level of scrutiny in determining the visa certification by OFLC as the applicants with prior job experience has 70% probability of getting their visa certified.

The OFLC can consider the employees who have completed a minimum education of Bachelor's for further scrutiny of visa certification.
