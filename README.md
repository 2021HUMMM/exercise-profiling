
# Before Profiling
## GUI JMeter Test Result
1. all-student-name: </br>
<img width="1280" alt="Results Table" src="https://github.com/user-attachments/assets/3c672b5e-a86c-4580-9e8e-9b50e7146c39" />
2. highest-gpa: </br>
<img width="1280" alt="Results Table" src="https://github.com/user-attachments/assets/b34dede1-3963-4701-a714-74187dba1c68" />
3. all-student: </br>
<img width="1280" alt="Results Table" src="https://github.com/user-attachments/assets/f3c8d6ae-3ae8-4237-9154-5f52f8b503ca" />


## Command Line JMeter Test Result 
1. all-student-name: </br>
<img width="1280" alt="all-students-name" src="https://github.com/user-attachments/assets/46c2ce05-d803-4ee2-b2de-92e6647bff23" />
2. highest-gpa: </br>
<img width="1280" alt="highest-gpa" src="https://github.com/user-attachments/assets/f8180224-21b7-495c-ab24-cd56ce77cf20" />
3. all-students: </br>
<img width="1280" alt="all-students" src="https://github.com/user-attachments/assets/d75ae395-297f-4d9f-89c8-d4c4103565b1" />

# After Profiling

## GUI JMeter Test Result
1. all-student-name: </br>
<img width="750" alt="Results Table" src="https://github.com/user-attachments/assets/30cef03f-5df3-4054-a7c7-dcae84d7c887" />
2. highest-gpa: </br>
<img width="748" alt="Results Table" src="https://github.com/user-attachments/assets/04419601-8603-4e84-a756-ddfa16e69ed0" />
3. all-students: </br>
<img width="752" alt="Results Table" src="https://github.com/user-attachments/assets/c839e9d4-144d-4ec9-93d8-ca7284468729" />
## Command Line JMeter Test Result 
1. all-student-name: </br>
<img width="1041" alt="Image" src="https://github.com/user-attachments/assets/449df730-e5b8-4677-a292-ad61c64835ab" />
2. highest-gpa: </br>
<img width="1010" alt="Image" src="https://github.com/user-attachments/assets/2e56559b-fa40-4cc1-af0a-a90849c1709b" />
3. all-students: </br>
<img width="1052" alt="Image" src="https://github.com/user-attachments/assets/b483e889-0f18-4ddc-97f4-d5cb2e7701d6" />

# Conclusion
As we can see, there's a huge improvement in performance after we have done profiling on the source code.
- all-student:
  - before profiling: around 40200ms
  - after profiling: around 1800ms
  - this is around 95.5% improvement
- all-student-name: 
  - before profiling: around 1500ms
  - after profiling: around 300ms
  - this is around 80% improvement
- highest-gpa:
  - before profiling: around 109ms
  - after profiling: around 46ms
  - this is around 57.8% improvement

After performing profiling and optimization, we achieved significant performance improvements across all queries. The all-student query showed the most dramatic improvement, 
reducing execution time by 95.5%, followed by all-student-name with an 80% improvement. Even the highest-gpa query, which was already relatively fast, saw a 57.8% reduction 
in execution time. These results highlight the effectiveness of profiling in identifying bottlenecks and optimizing code for better efficiency.

# Reflection
