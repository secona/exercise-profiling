# Performance Testing

## Endpoint `/all-student`

### Command Line Results
![image](https://github.com/user-attachments/assets/636f1b3c-a597-4cd1-82e6-2f9052a743ab)

### Before Optimization
![image](https://github.com/user-attachments/assets/34ab9d92-4782-40df-8c79-c24982f6db6e)

### After Optimization
![image](https://github.com/user-attachments/assets/12a87242-e965-4f97-bf09-bd6f8511f1f8)

## Endpoint `/all-student-name`

### Command Line Results
![image](https://github.com/user-attachments/assets/77f76362-9d4f-4f7d-aaff-af3587a8293b)

### Before Optimization
![image](https://github.com/user-attachments/assets/a75cc1d8-1061-4df8-b989-2ba7aefd25cb)

### After Optimization
![image](https://github.com/user-attachments/assets/be15a0f7-2c31-4800-ac0f-f901bde3368c)

## Endpoint `/highest-gpa`

### Command Line Results
![image](https://github.com/user-attachments/assets/5b343e7a-c114-4ba5-8f2f-a153528098d6)

### Before Optimization
![image](https://github.com/user-attachments/assets/1bf240b2-9641-49a1-936f-2a860813846a)

### After Optimization
![image](https://github.com/user-attachments/assets/d01afeef-7466-4ffc-8781-598842783fdc)

# Reflection

1. **What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?**

    JMeter is a load testing tool that simulates user traffic to evaluate how well the program handles high loads. It measures response times, throughput, and scalability.
    In contrast, Intellij Profiler focuses on code-level performance analysis, identifying CPU-heavy methods, memory leaks, and thread contention. While JMeter helps assess overall
    system performance under stress, IntelliJ Profiler provides insights into the specific parts of the code that contribute to performance bottlenecks.

3. **How does the profiling process help you in identifying and understanding the weak points in your application?**

    Profiling provides a detailed breakdown of resource consumption, highlighting inefficient methods and areas of high CPU or memory usage. For example, when profiling the `/all-students`
    endpoint, it showed that `getAllStudentsWithCourses` is consuming a significant amount of resources. This allows me to prioritize optimizing this method, ensuring a more efficient
    execution without wasting time on less impactful areas.

5. **Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?**

    Yes, IntelliJ Profiler is highly effective. It provides a clear visualization of performance metrics, such as CPU usage, memory allocation, and thread activity. By pinpointing which
    processes are consuming excessive resources, it enables developers to focus on optimizing critical areas, leading to better application performance.

7. **What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?**

    One of the main challenges is interpreting the profiling data effectively, as it requires familiarity with CPU sampling, memory allocation tracking, and thread analysis. Initially,
    it took time to understand the reports and differentiate between normal and problematic behavior. To overcome this, I approached the problem slowly while remembering my operating systems
    class.

9. **What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?**

    IntelliJ Profiler helps identify performance bottlenecks at a granular level, allowing for targeted optimizations. Key benefits include:
    - Identifying inefficient methods and reducing CPU/memory overhead.
    - Detecting memory leaks to improve application stability.
    - Analyzing thread activity to resolve concurrency issues.
    - Providing actionable insights that lead to measurable performance improvements.

10. **How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?**

    When profiling results differ from performance testing findings, I first verify that both tests are conducted under comparable conditions, including dataset size, load conditions, and system
    environment. If discrepancies persist, I analyze the execution context, JMeter tests high-level application behavior, while IntelliJ Profiler examines low-level code execution. I may also cross-check
    logs, use additional profiling tools, or conduct targeted experiments to isolate the root cause of inconsistencies.

12. **What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?**

    After identifying performance bottlenecks, I focus on optimizing the affected code by:

    - Improving algorithm efficiency and reducing redundant computations.
    - Optimizing database queries and reducing unnecessary data fetching.
    
    To ensure that these optimizations do not introduce new issues, I rely on unit tests and integration test. Automated testing validates functional correctness, while profiling before and after changes ensures performance
    improvements without regressions.
