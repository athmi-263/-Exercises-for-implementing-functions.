# -Exercises-for-implementing-functions.
def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    department = input("Enter Department: ")
    basic_salary = float(input("Enter Basic Salary: "))
    return name, emp_id, department, basic_salary


def calculate_salary(basic_salary):
    hra = basic_salary * 0.20
    da = basic_salary * 0.10
    pf = basic_salary * 0.12
    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf
    return hra, da, pf, gross_salary, net_salary


def print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net):
    print("\n======= EMPLOYEE SALARY SLIP ========")
    print("Employee Name :", name)
    print("Employee ID :", emp_id)
    print("Department :", department)
    print("--------------------------------------")
    print("Basic Salary     : Rs.", basic)
    print("HRA (20%)        : Rs.", hra)
    print("DA (10%)         : Rs.", da)
    print("PF Deduction     : Rs.", pf)
    print("--------------------------------------")
    print("Gross Salary     : Rs.", gross)
    print("Net Salary       : Rs.", net)
    print("======================================")



name, emp_id, department, basic = get_employee_details()
hra, da, pf, gross, net = calculate_salary(basic)
print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)


OUTPUT
            
Enter Employee Name: ATHMIKA
Enter Employee ID: 326
Enter Department: CS
Enter Basic Salary: 50000

======= EMPLOYEE SALARY SLIP ========
Employee Name : ATHMIKA
Employee ID : 326
Department : CS
--------------------------------------
Basic Salary     : Rs. 50000.0
HRA (20%)        : Rs. 10000.0
DA (10%)         : Rs. 5000.0
PF Deduction     : Rs. 6000.0
--------------------------------------
Gross Salary     : Rs. 65000.0
Net Salary       : Rs. 59000.0
