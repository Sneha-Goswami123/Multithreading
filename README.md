# Sneha (102303723)

# Multi-Threading Matrix Multiplication

## Objective
The objective of this assignment is to analyze the effect of multithreading (using multiprocessing in Python) on execution time and CPU utilization by performing large-scale matrix multiplication.

---

## Approach
- Random matrices of size 1000 × 1000 were generated
- Each matrix was multiplied with a constant matrix
- The operation was repeated for 500 matrices
- Multiprocessing was used to execute tasks in parallel
- Number of threads (processes) varied from:
  T = 1 to 2 × number of CPU cores

---

## Technologies Used
- Python
- NumPy
- Multiprocessing
- Matplotlib

---

## Experiment Details
- Each process performs matrix multiplication independently
- Execution time is measured for different thread counts
- A graph is plotted between:
  Number of Threads vs Execution Time

---

## Observations
- Execution time decreases initially as threads increase
- After reaching an optimal number of threads, performance fluctuates or slightly degrades
- This is due to overhead such as:
  - Context switching
  - Process management
  - CPU resource contention

---

## CPU Usage Analysis
- CPU utilization was observed using Task Manager
- Logical processors view was used to monitor individual cores
- Observations:
  - T = 1 → Only one core active
  - Increasing T → More cores utilized
  - Higher T → Near full CPU usage

---

## Challenges
- Original requirement of 5000 × 5000 matrices was not feasible due to hardware limitations
- Matrix size was reduced to 1000 × 1000 while maintaining computational behavior
- Minor fluctuations observed due to system background processes

---

## Results
<img width="1054" height="569" alt="image" src="https://github.com/user-attachments/assets/326b0a66-69dc-40de-9e6c-0d1fd2fcc44f" />




<img width="626" height="354" alt="image" src="https://github.com/user-attachments/assets/97562cdd-5a6b-455b-af08-1cdb5e5e0e61" />


---

## Conclusion
Multithreading improves performance up to a certain limit. Beyond that, increasing the number of threads leads to overhead and reduced efficiency. This demonstrates practical limitations of parallel processing.

---

## Additional Notes
- CPU graphs were captured manually using Task Manager
