# author: Rafael Salimov // https://github.com/thesaintraphael


import  math
import time


def put():
    a = None
    while a is None:
        try:
            a = float(input('Enter first number: '))
        except:
            print('Please enter a number')

    b = None
    while b is None:
        try:
            b = float(input('Enter second number: '))
        except:
            print('Please enter a number')

    return (a, b)




print ("""

******************************************

Welcome to kinda of Basic Calculator.

Operations:

1. Additon
2. Substratction
3. Multiplication
4. Division
5. Trigonometric calculations
6. Logarithmic calculations
7. Convert angle x from radians to degrees.

Type 'q' in order to end program.

******************************************

""")

time.sleep(1)
while True:

    n = input("Enter your choice: ")

    if n == '1':
        n = put()
        print("The sum of given numbers is", sum(n))

    elif n == '2':
        n = put()
        print("The difference between numbers is", n[0] - n[1])
    elif n == '3':
        n = put()
        print("The product of given numbers is", n[0] * n[1])
    elif n == '4':
        n = put()
        if n[0] % n[1] == 0:
            print("The bolme of given digits is:", n[0] // n[1])
        else:
            c = n[0] / n[1]
            print("The bolme of given gigits is %.2f" %c)

    elif n == '5':
        print ("""

        Operations:

        1. sinus
        2. cosinus
        3. tanges
        4. cotanges

        """)

        n = input("Select trigonometric function: ")

        if n == '1':
            a = float(input("Enter the degree in radians: "))
            print ("Answer: %.4f" %math.sin(a))
        elif n == '2':
            a = float(input("Enter the degree in radians: "))
            print ("Answer: %.4f" %math.cos(a))
        elif n == '3':
            a = float(input("Enter the degree in radians: "))
            print ("Answer: %.4f" %math.tan(a))
        elif n == '4':
            a = float(input("Enter the degree in radians: "))
            b = 1/ math.tan(a)
            print ("Answer: %.4f" %b)
        else:
            print("Wrong operation")
    elif n == '6':
            print("""

            1. Logarifm of the given base
            2. Log10

            """)
            n = input("Enter your choice: ")
            if n == '1':
                n = put()
                print ("Answer;", math.log(n[0], n[1]))
            elif n == '2':
                b = None
                while b is None:
                    try:
                        b = int(input("Enter an integer number: "))
                    except:
                        print('Please enter right input')
                        
                print ("Answer:", math.log10(b))
            else:
                print ("Wrong operation")
    elif n == '7':
        b = None
        while b is None:
            try:
                b = int(input("Enter an integer number: "))
            except:
                print('Please enter right input')
        print("{} radians is {} degrees".format(b, math.degrees(b)))

    elif n == 'q':
        print("Programdan cixilir")
        time.sleep(1)
        print('Proram is ended')
        break
    else:
        print("Wrong operation")




    
