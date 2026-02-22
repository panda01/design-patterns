# Design Patterns

A highly opinionated repo about design patterns, mainly in typescript / javascript.

## General Code Complexity

Generaly people interacting with code already have many things going on in their mind. As such you should write code so that it is as simple as possible for another human to interpret.

### Verbose naming
Name all of your functions, objects, classes, and constants with verbose names. The more verbose the name generally the better, in general the names should be simple sentences in that they have a subject and a verb. calculateSumOfCellsValue is better than calculateSum. 

### 3 levels of abstraction
Try and have no more than 3 levels of abstraction. 2 is preferable. too much more than that and a human is likely to lose track of what exactly every level does.

## Patterns vs Anti-Patterns

### If statements
99% if statements should have named conditions.

- Anti-Patterns
```
if (description === undefined) {
  // do something
}
if (score < 80) {
  // do something
}
```
- Patterns
```
const cantFindDescription = description === undefined;
if (cantFindDescription) {
  // do something
}
const scoreIsntPassing = score < 80;
if (scoreIsntPassing) {
  // do something
}
```
