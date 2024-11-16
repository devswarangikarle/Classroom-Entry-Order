# Classroom-Entry-Order

In a lively school, there were N students who entered the classroom one by one at different times. After each student entered, they shared how many students were already present before them. The i-th student mentioned that there were Aᵢ students in the class before they arrived. Now, the teacher, curious about the exact order in which the students entered, asked for help to figure out the correct sequence. Can you determine the order in which the students entered the classroom?

def classroom_entry_order(n, a):
    students = [(a[i], i + 1) for i in range(n)]
    
    students.sort()
    
    order = [student[1] for student in students]
    
    return order

n = int(input())
a = list(map(int, input().split()))

result = classroom_entry_order(n, a)
print(*result)
