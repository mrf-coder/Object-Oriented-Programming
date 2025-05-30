# Object-Oriented-Programming
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
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
