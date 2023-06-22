import random
import string

def generate_random_email():
    name = ''.join(random.choices(string.ascii_lowercase, k=8)) # генерация случайного имени
    domain = ''.join(random.choices(string.ascii_lowercase, k=6)) # генерация случайного домена
    local = ''.join(random.choices(string.ascii_lowercase, k=3)) # генерация случайной локальной части
    email = f"{name}@{domain}.{local}" # создание email адреса
    return email

import random

students = []

# функция для добавления студента в список
def add_student():
    name = input("Введите имя студента: ")
    surname = input("Введите фамилию студента: ")
    year = int(input("Введите год рождения студента: "))
    month = int(input("Введите месяц рождения студента: "))
    day = int(input("Введите день рождения студента: "))
    birthdate = (year, month, day)
    record_book = []
    subjects_number = int(input("Введите количество предметов в зачетке: "))
    for i in range(subjects_number):
        subject = input("Введите название предмета: ")
        exam_date = input("Введите дату экзамена: ")
        teacher = input("Введите ФИО преподавателя: ")
        grade = int(input("Введите оценку за экзамен: "))
        record_book.append((subject, exam_date, teacher, grade))
    student = {"name": name, "surname": surname, "birthdate": birthdate, "record_book": record_book}
    students.append(student)

# функция для получения оценок студента с наихудшей успеваемостью
def get_worst_grade(student):
    worst_grade = None
    for subject, exam_date, teacher, grade in student["record_book"]:
        if worst_grade is None or grade < worst_grade:
            worst_grade = grade
    return worst_grade

# функция для вывода информации о студенте с наихудшей успеваемостью
def show_worst_grade(student):
    name = student["name"]
    surname = student["surname"]
    worst_grade = get_worst_grade(student)
    for subject, exam_date, teacher, grade in student["record_book"]:
        if grade == worst_grade:
            print(f"{surname} {name} - {subject}: {grade}")

5def exercise_2():
    # заполнение списка студентов
    students_number = int(input("Введите количество студентов в группе: "))
    for i in range(students_number):
        print(f"Студент {i+1}:")
        add_student()

    # вывод информации о студенте с наихудшей успеваемостью
    worst_grade = None
    worst_student = None
    for student in students:
        grade = get_worst_grade(student)
        if worst_grade is None or grade < worst_grade:
            worst_grade = grade
            worst_student = student

    if worst_student is not None:
        show_worst_grade(worst_student)
    else:
        print("Список студентов пуст.")

try:
    choice = int(input("Выбери номер задачи(1 или 2) или отрицательное число для выхода:"))
except ValueError:
    print("Это не число")
    choice = None

if choice == 1:
    print("Первое задание")
    print("Сгенерированная почта в формате: <name>@<domen>.<local> - ", generate_random_email())

elif choice == 2:
    print("Второе задание")
    exercise_2()

elif isinstance(choice, int):
    print("Число находится вне диапазона")
