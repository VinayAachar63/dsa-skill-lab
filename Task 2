class StudentManager:
    def _init_(self):
        self.students = {}

    def add_student(self):
        n = int(input("Enter the number of students: "))
        for i in range(n):
            name = input(f"Enter the name of student {i+1}: ")
            marks1 = int(input(f"Enter marks 1 for {name}: "))
            marks2 = int(input(f"Enter marks 2 for {name}: "))
            marks3 = int(input(f"Enter marks 3 for {name}: "))
            self.students[name] = [marks1, marks2, marks3]

    def show_names(self):
        print("Student Names:")
        for name in self.students:
            print(name)

    def calculate_average(self):
        for name, marks in self.students.items():
            total = sum(marks)
            average = total / 3
            self.students[name].append(average)

    def rank_students(self):
        sorted_students = sorted(self.students.items(), key=lambda x: x[1][3], reverse=True)
        print("Student Ranking:")
        rank = 1
        for student in sorted_students:
            name = student[0]
            average = student[1][3]
            print(f"{rank}. {name} - Average: {average:.2f}")
            rank += 1
manager = StudentManager()
manager.add_student()
manager.show_names()
manager.calculate_average()
manager.rank_students()
