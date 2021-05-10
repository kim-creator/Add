
>>> a = [2, 4, 6, 8]
>>> len(a)
4
>>> for i, j in enumerate(a):
	print(i, j)

	
0 2
1 4
2 6
3 8
>>> for i in a:
	print(i)

	
2
4
6
8
>>> 
>>> 
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'a', 'i', 'j']
>>> del a[3]
>>> a
[2, 4, 6]
>>> a.remove(4)
>>> a
[2, 6]
>>> a.pop()
6
>>> a.append(3)
>>> a.append(5)
>>> a
[2, 3, 5]
>>> b = {'이름':'철수', '나이':20, '직업':'학생'}
>>> type(b)
<class 'dict'>
>>> 
>>> b.items()
dict_items([('이름', '철수'), ('나이', 20), ('직업', '학생')])
>>> 
>>> b.keys()
dict_keys(['이름', '나이', '직업'])
>>> 
>>> b.values()
dict_values(['철수', 20, '학생'])
>>> 
>>> for key, value  in  b.items():
	print(key, value)

	
이름 철수
나이 20
직업 학생
>>> dir(b)
['__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__ior__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__ror__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
>>> b['이름']
'철수'
>>> b['학년']
Traceback (most recent call last):
  File "<pyshell#33>", line 1, in <module>
    b['학년']
KeyError: '학년'
>>> b.popitem()
('직업', '학생')
>>> b
{'이름': '철수', '나이': 20}
>>> b.update({'고향':'부산시'})
>>> b
{'이름': '철수', '나이': 20, '고향': '부산시'}
>>> 
>>> 
>>> 

>>> def Add(x, y):
	return x+y

>>> Add(10, 30)
40

>>> 
>>> Add(20)
Traceback (most recent call last):
  File "<pyshell#46>", line 1, in <module>
    Add(20)
TypeError: Add() missing 1 required positional argument: 'y'
>>> 
>>> Add(20, 40, 60)
Traceback (most recent call last):
  File "<pyshell#48>", line 1, in <module>
    Add(20, 40, 60)
TypeError: Add() takes 2 positional arguments but 3 were given
>>> 
>>> 
>>> b
{'이름': '철수', '나이': 20, '고향': '부산시'}
>>> a
[2, 3, 5]
>>> a = [1, 2, 3, 4]
>>> sum(a)
10
>>> sum(1, 2, 3)
Traceback (most recent call last):
  File "<pyshell#55>", line 1, in <module>
    sum(1, 2, 3)
TypeError: sum() takes at most 2 arguments (3 given)
>>> sum([1, 2, 3])
6
>>> sum([1, 2, 3, 6])
12
>>> def mySum(*x):
	Sum = 0
	for i in *x:
		Sum = Sum + i
		
SyntaxError: can't use starred expression here
>>> def mySum(*x):
	Sum = 0
	for i in x:
		Sum = Sum + i

		
>>> mySum(2, 3, 4)
>>> def mySum(*x):
	Sum = 0
	for i in x:
		Sum = Sum + i
	return Sum

>>> mySum(2, 3, 4)
9
>>> mySum(2, 3, 4, 7, 9, 10)
35
>>> a
[1, 2, 3, 4]
>>> mySum(a)
Traceback (most recent call last):
  File "<pyshell#70>", line 1, in <module>
    mySum(a)
  File "<pyshell#66>", line 4, in mySum
    Sum = Sum + i
TypeError: unsupported operand type(s) for +: 'int' and 'list'
>>> a
[1, 2, 3, 4]
>>> mySum(1, 2, 3, 4)
10
>>> a
[1, 2, 3, 4]
>>> mySum(*a)
10
>>> mySum(2, 3, 4)
9
>>> 
>>> mySum(a)
Traceback (most recent call last):
  File "<pyshell#77>", line 1, in <module>
    mySum(a)
  File "<pyshell#66>", line 4, in mySum
    Sum = Sum + i
TypeError: unsupported operand type(s) for +: 'int' and 'list'

>>> a + 5
Traceback (most recent call last):
  File "<pyshell#78>", line 1, in <module>
    a + 5
TypeError: can only concatenate list (not "int") to list
>>> 5 + a
Traceback (most recent call last):
  File "<pyshell#79>", line 1, in <module>
    5 + a
TypeError: unsupported operand type(s) for +: 'int' and 'list'
>>> 
>>> 
>>> 
>>> def Add2(x=30, y=50):
	return x+y

>>> Add(100, 200)
300
>>> 
>>> Add(3)
Traceback (most recent call last):
  File "<pyshell#88>", line 1, in <module>
    Add(3)
TypeError: Add() missing 1 required positional argument: 'y'
>>> Add2(100, 200)
300
>>> Add2(3)
53
>>> Add2()
80
>>> Add2(y=100, x=200)
300
>>> 
>>> sum([2, 3])
5
>>> sum([2, 3, 4])
9
>>> sum([2, 3, 4, 9, 30, 3333])
3381
>>> sum(2, 3, 4)
Traceback (most recent call last):
  File "<pyshell#97>", line 1, in <module>
    sum(2, 3, 4)
TypeError: sum() takes at most 2 arguments (3 given)
>>> sum([2, 3, 4])
9
>>> mySum(2, 3)
5
>>> mySum(2)
2
>>> mySum(2, 1, 6)
9
>>> a
[1, 2, 3, 4]
>>> sum(a)
10
>>> mySum(a)
Traceback (most recent call last):
  File "<pyshell#104>", line 1, in <module>
    mySum(a)
  File "<pyshell#66>", line 4, in mySum
    Sum = Sum + i
TypeError: unsupported operand type(s) for +: 'int' and 'list'
>>> mySum(*a)
10
>>> a
[1, 2, 3, 4]
>>> mySum(1, 2, 3, 4)
10
>>> k = [3, 4, 5]
>>> mySum(*k)
12
>>> mySum(*dd)
Traceback (most recent call last):
  File "<pyshell#110>", line 1, in <module>
    mySum(*dd)
NameError: name 'dd' is not defined
>>> 
>>> 
>>> def Add5(x, y):
	return None

>>> Add(2, 3)
5
>>> def Add5(x, y):
	return None

>>> Add5(3, 4)
>>> r = Add5(3, 4)
>>> r
>>> def Add5(x, y):
	return x+y

>>> r = Add5(3, 4)
>>> r
7
>>> def Add5(x, y):
	return x+y, x-y, x*y

>>> r = Add5(3, 4)
>>> r
(7, -1, 12)
>>> type(r)
<class 'tuple'>



  




>>> aa = 1200
>>> aa == 1000
False
>>> aa + 30
1230
>>> aa
1200
>>> aa = aa + 30
>>> aa
1230
>>> aa += 30
>>> aa + 30
1290
>>> aa.__add__(30)
1290
>>> 
>>> aa.__eq__(1000)
False
>>> dir(aa)
['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', '__getattribute__', '__getnewargs__', '__gt__', '__hash__', '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 'as_integer_ratio', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 'real', 'to_bytes']
>>> 



