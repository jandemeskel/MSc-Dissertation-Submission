
# Framework guidance

## Preliminary

Firstly, before attempting to use the framework, please ensure all packages and dependecies are correctly installed as instructed in the documentation - 'Link to documentation here'


## Functionality

To access the modules, ensure the framework is correctly imported by using the following test:

<div align="center">
    <img src ="PathTest.png" width = 50% height = auto>
</div>

***If the test fails:***

- Revert back to the documentation to ensure installation was completed correctly.
- Ensure the with file structure resembles the recommended structure within the documentation to ensure pathing issues do not occur.


***If successful, the framework's features are ready to be used***

The following information contains the name of the module, the main class contained and the corresponding functionality.

<div align="center">

<strong>Module Name</strong>: Muller_input()
<br>
<strong>Class</strong>: NMA

| Function      | Description |                            
| ----------- | ----------- |                           
|||                            
|||                            
|||
</div>

<br>
<div align="center">

<strong>Module Name</strong>: NGA_conversion
<br>
<strong>Class</strong>: NGA(states, initial, alphabet, transitions, acceptance)

| Function      | Description |                            
| ----------- | ----------- |                           
|||                            
|||                            
|||


</div>
<br>
<div align="center">

<strong>Module Name</strong>: NBA_conversion
<br>
<strong>Class</strong>: NBA()

| Function      | Description |                            
| ----------- | ----------- |                           
|||                            
|||                            
|||

</div>
<br>
<div align="center">

<strong>Module Name</strong>: Regular_operations
<br>
<br>
<strong>Class</strong>: Union([Automata1, Automata2])

| Function      | Description |                            
| ----------- | ----------- |                           
|||                            
|||                            
|||

<strong>Class</strong>: Intersection([Automata1, Automata2])

| Function      | Description |                            
| ----------- | ----------- |                           
|||                            
|||                            
|||


</div>



## Data Structure

Every automata is stored within a nested array with the following structure:

```
Automata = [ [States], [Initial(s)], [Alphabet], [Transitions], [Accepting] ] 
```

Where the transitions array takes the form of:

``` 
Transition = [T1, T2, ..., Tn]
T1 = [Start, [computed chars], [End state]]
etc...
```


For instance, the following automata and the corresponding data struct used in the framework to model it.

<div align="center">
    <img src ="ExampleDataStruct.png" width = 35% height = auto>
</div>


```
A = [ [Q], [Q0], [E], [T], [AC]]

Q = [q0, q1]

Q0 = [q0]

E = [a]

T = [ [[q0], [a], [q1]], [[q1], [a], [q0]] ]

AC = [q1]
```


## Applications

Similar to the implementation of the union and intersection, a user may desire to implement the complement of an NGA. The user could do so by utilizing the framework and any standard algorithm as such:


<div align="center">
    <img src ="ExampleUse.png" width = 49% height = auto>
    <img src ="Complement.png" width = 45% height = auto>
</div>
                                                    
                                                
