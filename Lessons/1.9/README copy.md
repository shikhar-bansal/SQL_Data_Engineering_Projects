# Heading 1
## Heading 2
### Heading 3

[markdown cheat sheet](https://www.markdownguide.org/cheat-sheet)

normal  
**bold text**  
*italics*  
`this is code`  
- bullet 1  
- bullet 2  
- bullet 3
- bullet 4  

1. number 1
2. number 2  

[link text](https://www.google.com)  
  
![Alt Text](../../Images/1_1_Project1_EDA.png)    

```sql
select sd.skills,count(jpf.*) as demand_count
from skills_dim as sd
inner join skills_job_dim as sjd on 
sjd.skill_id = sd.skill_id  
inner join job_postings_fact as jpf on
jpf.job_id = sjd.job_id
where
    jpf.job_title_short = 'Data Engineer'
    and jpf.job_work_from_home = true
group by sd.skills
order by demand_count DESC
limit 10;
```

