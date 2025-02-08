# Pointers in C

* **Pointers are a way of manipulating values in data structures.**

***Example:*** 
<br> The structure 'Person' has characteristics of Name(char) and Age(int).

```c

#include <stdio.h>
#include <string.h>

// Define a structure (like a class)
typedef struct {
    char name[50];
    int age;
} Person; // Name of the Structure

// Function to display a person's details
void showPerson(Person *p) {
    printf("Name: %s, Age: %d\n", p->name, p->age);
}

// Main function
int main() {
    // Create a person object using the 'Person' Struct
    Person p1;
    
    // Initialize values
    strcpy(p1.name, "Keanu Reeves");  
    p1.age = 60;
    
    // Call function with a pointer
    showPerson(&p1);
    
    return 0;
}

```
Manipulating structs can be confusing, so to simplify:
* When initalizing values: <br>
    * Char: **strcpy(\<Object> . \<charVariable>, "\<value>");** <br>
    * Numercials: **\<Object> . \<numericalVariable> = \<value>;** <br>
* When calling a method/function, we use ' & ': <br>
    * **function(& \<Object>);** <br>
* When defining parameters, we use ' * ': <br>
    * **function(\<Struct> \* \<Object>)** <br>
* When calling the parameters, we use ' -> ': <br>
    * **\<Object> -> \<Variable>;**







