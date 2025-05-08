## 1. What is the use of the keyof keyword in TypeScript? Provide an example.


In TypeScript, we can use keyof to extract all the keys of a type.

What benefits can we get from this?

It tells us in advance if we enter the wrong key.
It is useful for checking the type of functions.
The code is correct.


**For example**
```ts
type Person = {
  name: string;
  age: number;
};

type PersonKeys = keyof Person;
```
Here PersonKeys can just mean "name" or "age". Anything beyond that will be captured by TypeScript.



## 2. Provide an example of using union and intersection types in TypeScript.
 
# union type

 Union means — "or" "|" . It means that a variable can be any one of multiple types.

 **Example**
```ts
type ID = string | number;

let userId: ID;

userId = "abc123"; 
userId = 101; 
```

# intersection type

Intersection means — "and" "&" . It means that a variable must have multiple types of properties together.
**Example**
```ts
type Name = { name: string };
type Age = { age: number };

type Person = Name & Age;

const student: Person = {
  name: "Hasan",
  age: 20,
};
```
Here, both name and age must be given in the student field. If you give one less, TypeScript will catch an error.

