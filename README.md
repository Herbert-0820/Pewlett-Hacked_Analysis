# Overview of the analysis

In order to determine the number of retiring employees per title and identiify employees who are qufilied for mentorship prohram, the deeper processes have been done.

# Results

![alt text](https://github.com/Herbert-0820/School_District_Analysis/blob/main/Screen%20Shot%202021-09-24%20at%209.00.40%20PM.png)

32452 staff
29415 Senior Engineer
14221 Engineer
8047 Senior Staff
4502 Technique Leader
1761 Assistant Enginner

# Summary

Select Distinct ON(e.emp_no) e.emp_no,
  e.first_name,
  e.last_name,
  e.birth_date,
  de.from_date,
  de.to_date,
  t.title
  
  
  
  From employees as e
  left outer join dept_emp as de
  ON (e.emp_no = de.emp_no)
  left outer join titles as t
  ON (e.emp_no = t.emp_no)
  where (e.birth_date Between '1965-01-01' and '1965-12-31')
  order by e.empo;
  
  The code will show how many roles need to be filled out and  who are eligible to participate in a mentorship program
