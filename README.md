# CT421-AI--Genetic-Algorithm-for-Exam-Timetabling

**Author:** Ya Li Lin (22721291)  
**Date:** February 2026

---

## Files Included

- `exam_timetabling_GA-checkpoint.ipynb` - Main implementation
- `test_case1.txt` - Test instance (8 exams, 4 slots, 15 students)
- `small-2.txt` - Test instance (15 exams, 9 slots, 30 students)
- `medium-1.txt` - Test instance (25 exams, 10 slots, 60 students)
- `README.md` - This file

---

## How to Run

1. Open `exam_timetabling_GA-checkpoint.ipynb` in Jupyter Notebook
2. Run all cells sequentially from top to bottom
3. To test different instances, change the filename in Section 2

**Requirements:** Python 3.8+, numpy, matplotlib

---

## Code Structure

### Section 1-2: Setup & Data Loading
- Import libraries
- `read_instance()` - Parse input files

### Section 3: Solution Representation
- `create_random_solution()` - Generate chromosomes as integer arrays

### Section 4-7: Fitness Evaluation
- `count_hard_conflicts()` - Count student exam conflicts
- `count_consecutive_exams()` - Count consecutive exam violations
- `evaluate_fitness()` - Calculate weighted fitness score

### Section 8-10: Genetic Operators
- `tournament_selection()` - Select parents (tournament size 3)
- `uniform_crossover()` - Create offspring (50% from each parent)
- `mutate()` - Apply random mutations (5% rate)

### Section 11: Main Algorithm
- `run_ga()` - Execute genetic algorithm
  - Population: 100
  - Generations: 500
  - Crossover rate: 0.8
  - Mutation rate: 0.05
  - Elitism: 2 best solutions preserved

### Section 12-13: Results & Visualization
- Display convergence graphs
- Show timetable solutions

### Section 14: Parameter Testing
- Compare different mutation rates
- Multiple runs for statistical analysis

---

## Algorithm Parameters

| Parameter | Value |
|-----------|-------|
| Population Size | 100 |
| Generations | 500 |
| Crossover Rate | 0.8 |
| Mutation Rate | 0.05 |
| Tournament Size | 3 |
| Elitism | 2 |

---

## Results

All test instances achieved valid solutions (0 hard constraint violations):

- **test_case1:** Fitness = -22 (22 soft violations)
- **small-2:** Fitness = -30 (30 soft violations)  
- **medium-1:** Fitness = -77 (77 soft violations)

See full report PDF for detailed analysis.
