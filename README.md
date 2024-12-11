# Practical_1
Practical_1

File: /home/ubuntu/prac1dsl.py Page 1 of 1
# Score of student
marklist = [20, 50, 40, 50, 90, 50, 90, 90, None, 89, None]
# n = int(input("Enter no of students "))
# for i in range(n):
# # mark = int(input(f"Enter marks{i+1} student :"))
# marklist.append(mark)
# print(marklist)
total = 0
absent_student = 0
freq = {
}
max_val = marklist[0]
min_val = marklist[0]
for mark in marklist:
if mark == None:
absent_student += 1
else:
total += mark
# calculate Max and min marks
if mark < min_val:
min_val = mark
if max_val < mark:
max_val = mark
if mark != None:
if freq.get(mark) == None:
freq[mark] = 1
else:
freq[mark] += 1
print(f"a.Average Score of the class = {total/len(marklist)}")
print(f"b.Highest Score = {max_val} and Lowest Score = {min_val}")
print(f"c. Number of absent student = {absent_student}")
highest_freq = 0
highest_freq_mark = 0
for mark in freq:
if freq[mark] > highest_freq:
highest_freq = freq[mark]
highest_freq_mark = mark
print(f"d. Mark with highest frequency : {highest_freq_mark}")
#############################################################################
Output : -
ubuntu@ubuntu-Vostro-460:~/DSL$ /bin/python3 /home/ubuntu/DSL/Practical1.py
a.Average Score of the class = 51.72727272727273
b.Highest Score = 90 and Lowest Score = 20
c. Number of absent student = 2
d. Mark with highest frequency : 20
