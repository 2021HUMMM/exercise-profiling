
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

## 1. Difference between JMeter and IntelliJ Profiler in Performance Optimization
JMeter is primarily used for **load testing** and **performance benchmarking** by simulating multiple users interacting with an application, helping to identify scalability 
issues. On the other hand, IntelliJ Profiler is a **code-level performance analysis tool** that helps pinpoint bottlenecks in the code by analyzing CPU usage, memory allocation, and 
execution time. While JMeter focuses on external performance factors under different loads, IntelliJ Profiler provides deeper insights into **internal code inefficiencies**.

## 2. How Profiling Helps Identify Weak Points
Profiling helps by **tracking execution time**, **CPU usage**, and **memory consumption** of different parts of the code. It allows developers to visualize **which functions or operations are consuming the most resources**, helping them optimize the most critical parts of the application.

## 3. Effectiveness of IntelliJ Profiler in Identifying Bottlenecks
Yes, IntelliJ Profiler is highly effective in identifying bottlenecks as it provides **detailed insights into function calls, execution times, memory leaks, and CPU utilization**. It highlights inefficient code sections, making it easier to optimize application performance.

## 4. Challenges in Performance Testing and Profiling
Some common challenges include:
- **High overhead**: Profiling tools may introduce additional load, affecting performance.
- **Interpreting results**: Identifying the root cause of slowdowns can be complex.
- **Inconsistent results**: Performance may vary depending on environment settings.

To overcome these, it's important to:
- Run profiling in **controlled environments**.
- Use **multiple test runs** to confirm findings.
- Compare **profiling data with real-world performance metrics**.

## 5. Benefits of Using IntelliJ Profiler
- **Pinpoints performance bottlenecks** at the code level.
- **Helps in memory leak detection**, preventing crashes.
- **Optimizes CPU usage**, leading to faster execution times.
- **Provides real-time performance insights** to make informed optimizations.

## 6. Handling Inconsistencies Between IntelliJ Profiler and JMeter Results
If profiling results differ from JMeter findings:
- **Verify test environments** to ensure consistency.
- **Analyze different scenarios** (e.g., profiling focuses on single execution, while JMeter tests under load).
- **Cross-check with logs and metrics** to understand discrepancies.
- **Combine both approaches** for a comprehensive optimization strategy.

## 7. Strategies for Optimizing Code Without Affecting Functionality
- **Identify critical bottlenecks** and optimize only necessary parts, like i did with the methods on StudentService.
- **Refactor inefficient loops and queries** to improve execution time. I've done this in getAllStudentsWithCourse() and simplify
the code to just:
```java
public List<StudentCourse> getAllStudentsWithCourses() {
  return studentCourseRepository.findAll();
  }
 ```
- **Test after each change** to ensure functionality remains intact.
- **Monitor performance before and after optimizations** to measure impact.