# Object-Oriented-Programming

- __[Python-Conditionals](https://github.com/mrf-coder/Python-Conditionals.git)__ - 
- __[Python-Loops](https://github.com/mrf-coder/Python-Loops.git)__ - 
- __[Python-Eceptions ](https://github.com/mrf-coder/Python-Eceptions.git)__ - 
- __[Python-Libraries ](https://github.com/mrf-coder/Python-Libraries.git)__ - 
- __[Python-UnitTest ](https://github.com/mrf-coder/Python-UnitTest.git)__ - 
- __[Python-I-o](https://github.com/mrf-coder/Python-I-o.git)__ - 
- __[Regular-Expressions ](https://github.com/mrf-coder/Regular-Expressions.git)__ - 
- __[Object-Oriented-Programming](https://github.com/mrf-coder/Object-Oriented-Programming.git)__ - 
- __[Et-Cetera](https://github.com/mrf-coder/Et-Cetera.git)__ - 


```js
name = input("Name:")
house = input("House:")
print(f"{name} from {house}")
```
```js
def main():
    name = get_name()
    house = get_house()
    print(f"{name} from {house}")
def get_name():
    return input("Name:") 
def get_house():
    return input("House:") 

if __name__ == "__main__":
    main()

```
```js
def main():
    name,house = get_students()
    print(f"{name} from {house}")
def get_students():    
    n = input("Name:")
    h= input("House:") 
    return n,h
if __name__ == "__main__":
    main()

```
```js
def main():
    students = get_students()
    print(f"{students[0]} from {students[1]}")
def get_students():    
    n = input("Name:")
    h= input("House:") 
    return (n,h) #tuple
if __name__ == "__main__":
    main()

```
```js
def main():
    if students[0]=="Ron":
        students[1]="Ravenclaw"
    students = get_students()
    print(f"{students[0]} from {students[1]}")
def get_students():    
    n = input("Name:")
    h= input("House:") 
    return (n,h) #tuple  or [n,h]
if __name__ == "__main__":
    main()

```
```js
def main():
    students = get_students()
    print(f"{students['name']} from {students['house']}")
def get_students():  
    students = {}
    students["name"] = input("Name:")
    students ["house"]= input("House:") 
    return (students) #tuple
if __name__ == "__main__":
    main()

```
```js
def main():
    students = get_students()
    print(f"{students['name']} from {students['house']}")
def get_students():  
    name= input("Name:")
    house= input("House:") 
    return {"name":name,"house":house} #tuple
if __name__ == "__main__":
    main()

```
```js
def main():
    students = get_students()
    if students ["name"]=="Ron":
        students["house"]="Ravenclaw"
    print(f"{students['name']} from {students['house']}")
def get_students():  
    name= input("Name:")
    house= input("House:") 
    return {"name":name,"house":house} #tuple
if __name__ == "__main__":
    main()

```
```js
class Students:
    ... 
def main():
    students = get_students()
    print(f"{students.name} from {students.house}")
def get_students():
    students = Students()  
    students.name= input("Name:")
    students.house= input("House:") 
    return students #tuple
if __name__ == "__main__":
    main()

```
```js
class Students:
    def __init__(self, name, house):  # Fixed __init__ definition
        self.name = name
        self.house = house

def main():
    students = get_students()
    print(f"{students.name} from {students.house}")  # Accessing attributes
def get_students():
    name = input("Name: ")
    house = input("House: ")
    students = Students(name, house)  # Creating a Students object
    return students  # Returning the object, not a tuple
if __name__ == "__main__":
    main()
11:26
```
```js
class Students:
    def __init__(self, name, house): 
        if not name:
            raise ValueError("Missing name")
        if house not in ["house33", "house22", "house11", "house44"]:
            raise ValueError("Invalid house")
        self.name = name
        self.house = house
def main():
    students = get_students()
    print(f"{students.name} from {students.house}")  # Accessing attributes
def get_students():
    name = input("Name: ")
    house = input("House: ")
    return Students(name, house)  # Creating a Students object
if __name__ == "__main__":
    main()

```
```js
class Students:
    def __init__(self, name, house): 
        if not name:
            raise ValueError("Missing name")
        if house not in ["house33", "house22", "house11", "house44"]:
            raise ValueError("Invalid house")
        self.name = name
        self.house = house
   # def __str__(self):
       # return "a student"
    def __str__(self):
        return f"{self.name} from {self.house}"

# __str__ is NOT defined, so memory address will be shown

def get_students():
    name = input("Name: ").strip()
    house = input("House: ").strip()
    return Students(name, house)

def main():
    try:
        student = get_students()
        print(student)  # This will print memory address
    except ValueError as e:
        print("Error:", e)

if __name__ == "__main__":
    main()
12
```
```js
class Students:
    def __init__(self, name, house): 
        if not name:
            raise ValueError("Missing name")
        self.name = name
        self.house = house

    def __str__(self):
        return f"{self.name} from {self.house}"
   
    #Getter
    @property
    def house(self):
        return self._house
    
    #Setter
    @house.setter
    def house(self, house):
        if house not in ["house1", "house2", "house3", "house4"]:
            raise ValueError("Invalid house")
        self._house = house


def get_students():
    name = input("Name: ").strip()
    house = input("House: ").strip()
    return Students(name, house)

def main():
    try:
        student = get_students()
        print(student)
    except ValueError as e:
        print("Error:", e)

if __name__ == "__main__":
    main()

```
```js
class Students:
    def __init__(self, name, house): 
        self.name = name
        self.house = house

    def __str__(self):
        return f"{self.name} from {self.house}"

    # Getter for house
    @property
    def house(self):
        return self._house

    # Setter for house
    @house.setter
    def house(self, house):
        if house not in ["house1", "house2", "house3", "house4"]:
            raise ValueError("Invalid house")
        self._house = house

    # Getter for name
    @property
    def name(self):
        return self._name

    # Setter for name
    @name.setter
    def name(self, name):
        if not name:
            raise ValueError("Missing name")
        self._name = name


def get_students():
    name = input("Name: ").strip()
    house = input("House: ").strip()
    return Students(name, house)
def main():
    try:
        student = get_students()
        print(student)
    except ValueError as e:
        print("Error:", e)
if __name__ == "__main__":
    main()

```
##### class int(x , base=10 )
##### class str(objcet='')  srt.lower()  str.strip([char])
##### class list([iterable ])   list.append() // Dict a object  12:31
```js
class Hat:
  def sort(self,name)  :
    print(name,"in hostal no 2")


hat = Hat()
hat.sort("Harry")    
```
```js
import random

class Hat:
    def __init__(self): 
        self.hotel = ["hostal1", "hostal2", "hostal3", "hostal4"]

    def sort(self, name):
        print(name, "in the ", random.choice(self.hotel)) 

hat = Hat()
hat.sort("Harry")

```
```js
import random

class Hat:
    hotel = ["hostal1", "hostal2", "hostal3", "hostal4"]
    @classmethod
    def sort(cls, name):
        print(name, "in the ", random.choice(cls.hotel))  # Fixed: "choise" ➝ "choice"

Hat.sort("Harry")

```
```js
class Student:
    def __init__(self, name, house):
        self.name = name
        self.house = house

    def __str__(self):
        return f"{self.name} from {self.house}"

    @classmethod
    def get(cls):
        name = input("Name: ") 
        house = input("House: ")
        return cls(name, house)


def main():
    student = Student.get()
    print(student)


if __name__ == "__main__":  # Fixed: used == instead of =
    main()

```
```js
class Wizard:
    def __init__(self,name):
        if not name:
          raise ValueError("Missing name")
        self.name= name



class Student(Wizard):
   def __init__(self,name,house):
      super().__init__(name)
      self.house=house

class Professor(Wizard):
   def __init__(self,name,subject):
      super().__init__(name)
      self.subject=subject
wizard = Wizard("Albus")
student = Student("Harry","house33")
professor= Professor("Severus","Defence Againt the Dark Art")


```
```js
  Print Adress
class Vault:
    def __init__(self,galleons=0,sickles=0,knuts=0):
        self.galleons=galleons
        self.sickles=sickles
        self.knuts=knuts


potter=Vault(100,50,25)
print(potter)        

```
```js
class Vault:
    def __init__(self,galleons=0,sickles=0,knuts=0):
        self.galleons=galleons
        self.sickles=sickles
        self.knuts=knuts
    def __str__(self):
        return f"{self.galleons} Galleons {self.sickles} Sickles {self.knuts} Knuts " 

potter=Vault(100,50,25)
print(potter)        

```
```js
class Vault:
    def __init__(self,galleons=0,sickles=0,knuts=0):
        self.galleons=galleons
        self.sickles=sickles
        self.knuts=knuts
    def __str__(self):
        return f"{self.galleons} Galleons {self.sickles} Sickles {self.knuts} Knuts " 

potter=Vault(100,50,25)
print(potter)        

harry=Vault(15,544,250)
print(harry)        

```
```js
class Vault:
    def __init__(self,galleons=0,sickles=0,knuts=0):
        self.galleons=galleons
        self.sickles=sickles
        self.knuts=knuts
    def __str__(self):
        return f"{self.galleons} Galleons {self.sickles} Sickles {self.knuts} Knuts " 

potter=Vault(100,50,25)
print(potter)        

harry=Vault(150,100,25)
print(harry)        

galleons= potter.galleons+harry.galleons
sickles= potter.sickles+harry.sickles
knuts=potter.knuts+harry.knuts

total = Vault(galleons,sickles,knuts)
print(total)

```
###### object.__add__(self,other)
```js
class Vault:
    def __init__(self,galleons=0,sickles=0,knuts=0):
        self.galleons=galleons
        self.sickles=sickles
        self.knuts=knuts
    def __str__(self):
        
        return f"{self.galleons} Galleons {self.sickles} Sickles {self.knuts} Knuts " 
    def __add__(self,other):
        galleons= self.galleons+other.galleons
        sickles= self.sickles+other.sickles
        knuts=self.knuts+other.knuts
        return Vault(galleons,sickles,knuts)
potter=Vault(100,50,25)
print(potter)        

harry=Vault(150,100,25)
print(harry)        

total = potter+harry
print(total)

```
- __[Python-Conditionals](https://github.com/mrf-coder/Python-Conditionals.git)__ - 
- __[Python-Loops](https://github.com/mrf-coder/Python-Loops.git)__ - 
- __[Python-Eceptions ](https://github.com/mrf-coder/Python-Eceptions.git)__ - 
- __[Python-Libraries ](https://github.com/mrf-coder/Python-Libraries.git)__ - 
- __[Python-UnitTest ](https://github.com/mrf-coder/Python-UnitTest.git)__ - 
- __[Python-I-o](https://github.com/mrf-coder/Python-I-o.git)__ - 
- __[Regular-Expressions ](https://github.com/mrf-coder/Regular-Expressions.git)__ - 
- __[Object-Oriented-Programming](https://github.com/mrf-coder/Object-Oriented-Programming.git)__ - 
- __[Et-Cetera](https://github.com/mrf-coder/Et-Cetera.git)__ - 


