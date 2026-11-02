# International Students Mental Health SQL Analysis
An exploratory data analysis project using SQL to examine the mental health scores of international students based on their length of stay.

## 📊 Overview
This project analyzes how the duration of stay affects various mental health and psychological metrics among international students. The dataset helps evaluate depression scores (PHQ-9), social connectedness (SCS), and acculturative stress (AS) over time.

## 💻 SQL Query
```sql
SELECT 
    stay, 
    COUNT(inter_dom) AS count_int, 
    ROUND(AVG(todep), 2) AS average_phq, 
    ROUND(AVG(tosc), 2) AS average_scs, 
    ROUND(AVG(toas), 2) AS average_as
FROM 
    students
WHERE 
    inter_dom = 'Inter'
GROUP BY 
    stay
ORDER BY 
    stay DESC;
