#various places to declare static variables

class Test:
    a=10                     #we can declare within the class directly but from out side of any method
    def __init__(self):
        Test.b=20            #Inside constructor by using class name
    def m1(self):
        Test.c=30            #Inside instance method by using class name
    @classmethod
    def m2(cls):
        cls.d1=40            #Inside classmethod by using either class name or cls variable
        Test.d2=400
    @staticmethod
    def m3():
        Test.e=50            #Inside static method by using class name
print(Test.__dict__)
t=Test()
print(Test.__dict__)
t.m1()
print(Test.__dict__)
Test.m2()
print(Test.__dict__)
Test.m3()
print(Test.__dict__)
Test.f=60
print(Test.__dict__)

        
