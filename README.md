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
```js
```
```js
```
```js
```
```js
```
