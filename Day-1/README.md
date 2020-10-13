# Week-5 -- Day-1

## JavaScript Exercises

Becoming a web-developer will (should) involve solving a heavy amount of JavaScript challenges. The reason is two-fold. One is it will make you a better coder and two it will prepare you for the technical aspect of a job interview. So solve as many JavaScript challenges as you can while you are going through this bootcamp. Practice really does make master especially in this case!

![It's called practice - Obama](https://media.giphy.com/media/l0HlzD5PQGJYZ0Szu/giphy.gif)

### Challenge Breakdown

Breakdown each challenge into the following format:

    // What is the function asking for?

    // What is the name of the function     -->     
    // What is the number of arguments      -->    
    // What are the argument types          -->      
    // What are the argument name/s         -->      
    // What is the return type              -->     

    // Write the actual function definition here  

    // Call on / test the function here  


### Example:

**// What is the function asking for?**

*Americans are odd people: in their buildings, the first floor is actually the ground floor and there is no 13th floor (due to superstition).
Write a function that given a floor in the american system returns the floor in the european system.
With the 1st floor being replaced by the ground floor and the 13th floor being removed, the numbers move down to take their place. In case of above 13, they move down by two because there are two omitted numbers below them.
Basements (negatives) stay the same as the universal level.*

*Examples input outputs*

```
1  =>  0
0  =>  0
5  =>  4
15  =>  13
-3  =>  -3
```

**// What is the name of the function       -->** euroFloor     
**// What is the number of arguments     -->** 1    
**// What are the argument types             -->**  number    
**// What are the argument name/s         -->**  floor    
**// What is the return type                        -->**  number


**// Write the actual function definition here**

    function euroFloor(floor){
    	let euroFloor = floor;
    	// Pretending 13 does not exist :)
    	if(floor > 0 && floor < 13){
    		euroFloor = floor -1;
    	}else if (floor > 13){
	    	euroFloor = floor -2;
       }
       return euroFloor;
    }

**// Call on / test the function here**

    let newFloor = euroFloor(1);
    console.log("for floor #1: " + newFloor);

    newFloor = euroFloor(0);
    console.log("for floor #0: " + newFloor);

    newFloor = euroFloor(5);
    console.log("for floor #5: " + newFloor);

    newFloor = euroFloor(15);
    console.log("for floor #15: " + newFloor);

    newFloor = euroFloor(-3);
    console.log("for floor #-3: " + newFloor);
