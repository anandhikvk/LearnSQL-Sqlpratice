# LearnSQL-SqlPractice
DESCRIPTION:
LearnSQL is a website that helps to solve basic to advanced-level SQL queries. It has easy, medium, and hard level questions. It covers various topics like CASE, JOINS, GROUPBY, AGGREGATE FUNCTIONS, etc. It is a very beginner-friendly practice website for SQL Learners. 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Questions:
1. Show first name, last name, and gender of patients whose gender is 'M'.

```select first_name, last_name,gender from patients where gender='M'```

2. Show the first names of patients that start with the letter 'C'.
```select first_name from patients where first_name like 'C%'```

3. Update the patients table for the allergies column. If the patient's allergies are null, then replace them with 'NKA.'
```update patients set allergies='NKA' where allergies is null```

4.Show first name and last name concatinated into one column to show their full name.
```select concat(first_name,' ',last_name) from patients```

5.Show first name, last name, and the full province name of each patient.
```select p.first_name,p.last_name,pn.province_name from patients as p join province_names as pn on p.province_id=pn.province_id```

6.Show how many patients have a birth_date with 2010 as the birth year.
```select count(*) from patients where year(birth_date)=2010```

7.Show the first_name, last_name, and height of the patient with the greatest height.
```select first_name,last_name,max(height) from patients``` OR
```select firname,lastname,height from patients where height=(select max(height) from patients)```

8.Show all columns for patients who have one of the following patient_ids:1,45,534,879,1000
```select * from patients where patient_id in (1,45,534,879,1000)```

9.Show the total number of admissions
```select count(*) from admissions```

10.Show all the columns from admissions where the patient was admitted and discharged on the same day.
```select * from admissions where admission_date=discharge_date```


