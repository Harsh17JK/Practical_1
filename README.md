
# Score of student
marklist = [20, 50, 40, 50, 90, 50, 90, 90, None, 89, None]

total = 0
absent_student = 0
freq = {}
max_val = marklist[0]
min_val = marklist[0]

for mark in marklist:
    if mark is None:
        absent_student += 1
    else:
        total += mark
        # Calculate Max and Min marks
        if mark < min_val:
            min_val = mark
        if max_val < mark:
            max_val = mark
        # Track the frequency of each mark
        if mark not in freq:
            freq[mark] = 1
        else:
            freq[mark] += 1

# Calculate average score
average_score = total / (len(marklist) - absent_student)

# Find the mark with the highest frequency
highest_freq = 0
highest_freq_mark = 0
for mark in freq:
    if freq[mark] > highest_freq:
        highest_freq = freq[mark]
        highest_freq_mark = mark

# Display results
print(f"a. Average Score of the class = {average_score}")
print(f"b. Highest Score = {max_val} and Lowest Score = {min_val}")
print(f"c. Number of absent students = {absent_student}")
print(f"d. Mark with highest frequency: {highest_freq_mark}")
```

### Explanation:
- **Absent Students**: The program counts the `None` values in `marklist` to track how many students were absent.
- **Total**: It sums up all the scores while ignoring the `None` values.
- **Max and Min Values**: It calculates the highest and lowest marks.
- **Frequency**: The program tracks how many times each score appears in the list using a dictionary (`freq`).
- **Average Score**: The total score is divided by the number of students who have valid scores (ignoring `None` values).

