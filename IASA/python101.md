# Python gotcha

- python tem um comportamento estranho quando lidamos com parametros default de funções que são mutáveis (e.g. listas, dicionários, etc.)
  - Isto acontece porque o valor default é avaliado apenas uma vez, quando a função é definida, e não cada vez que a função é chamada.
  - Logo o mesmo objeto é partilhado entre todas as chamadas da função.
  
```python
def createStudent(name, age, grades=[]):
    return {
        'name': name,
        'age': age,
        'grades': grades
    }

chrisley = createStudent('Chrisley', 15)
dallas = createStudent('Dallas', 16)

def addGrade(student, grade):
    student['grades'].append(grade)
    # To help visualize the grades we have added a print statement
    print(student['grades'])

addGrade(chrisley, 90)
addGrade(dallas, 100)

```

O output deste código é:

```
[90]
[90, 100]
```

Apesar do esperado ser:

```
[90]
[100]
```

Para resolver isto devemos por exemplo usar `None` como valor default para indicar que nenhum valor foi passado e criar um novo objeto dentro da função.

```python
def createStudent(name, age, grades=None):
  if grades is None:
    grades = []
  return {
    'name': name,
    'age': age,
    'grades': grades
  }

def addGrade(student, grade):
    student['grades'].append(grade)
    # To help visualize the grades we have added a print statement
    print(student['grades'])

chrisley = createStudent('Chrisley', 15)
dallas = createStudent('Dallas', 16)

addGrade(chrisley, 90)
addGrade(dallas, 100)
```

Isto já produz o output esperado:

```
[90]
[100]
```

