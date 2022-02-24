"# Coding-Assignment-Week3" 

//Create an array called ages that contains the following values: 3, 9, 23, 64, 2, 8, 28, 93.//
//Programmatically subtract the value of the first element in the array from the value in the last element of the array (do not use numbers to reference the last element,
// find it programmatically, ages[7] – ages[0] is not allowed). Print the result to the console.//
//Use a loop to iterate through the array and calculate the average age. Print the result to the console.

var ages = [3, 9, 23, 64, 2, 8, 28, 93]
ages.push(20)                    
var sum= 0, avg = 0.0
for(var i=0; i < ages.length; i++){      
    sum = sum + ages[i] 
    console.log(sum);      //When I call it add all of the numbers together to end at a total of 250. 
}
avg = sum / ages.length  //Using ages.length to find the average of the number of letters found in the array. 
console.log(avg)

var last = ages[ages.length - 1] 
var first = ages[ages.length - ages.length] 
diff = last - first 

console.log(`Difference between first and last element is: ${diff}`)

//Create an array called names that contains the following values: ‘Sam’, ‘Tommy’, ‘Tim’, ‘Sally’, ‘Buck’, ‘Bob’.//

//Use a loop to iterate through the array and calculate the average number of letters per name. Print the result to the console.//
//Use a loop to iterate through the array again and concatenate all the names //

var names = ['Sam', 'Tommy', 'Tim', 'Sally', 'Buck', 'Bob'];
sum=0;
for(i=0; i < names.length; i++){
    sum=sum + names[i].length;
}console.log('Letters per name:',sum/names.length);

const merge = (names) => {
    for (let i=0; i<names.length; i++)
    return names
}
console.log(merge(names));


var nameLengths = [];             //created a new variable to represent the name lengths and the numbers or each name. 

    for(i=0; i<names.length; i++){
        nameLengths[i] = names[i].length;   //The i is all of the names in the array that will be used. 
    }
    console.log(nameLengths);

    sum=0;

    for(i=0; i<nameLengths.length; i++){   //created another loop to find the sun
        sum += nameLengths[i];
    }

    console.log("The Sum is: ",sum);


//you can access the last element of an array using 
//you can access the first element of an array using

//Write a function that takes two parameters, word and n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in ‘Hello’ and 3, I would expect the function to return ‘HelloHelloHello’).//
function concat_n_time(word,n)
{
var con= word;
for (i=1; i<=n; i++)
{
    con= con.concat(word);
}
return con;
}
console.log("Concatenated words:", concat_n_time("Hello",2));
console.log("\n\n\n");


//Write a function that takes two parameters, firstName and lastName, and returns a full name (the full name should be the first and the last name separated by a space).


function fullName(firstName, lastName){       //created a function with two parameters firstName and LastName
    console.log(firstName + " " + lastName);
}
fullName('Sarah', 'Carlos')                    //printed my full name to be called



//Write a function that takes an array of numbers and returns true if the sum of all the numbers in the array is greater than 100.//
var arr= [5, 8, 10, 40, 35, 15]    //created a random array of numbers

function numbers(arr){
    sum = 0;
    for(i=0; i<arr.length; i++) {      
         sum=sum+arr[i];            //Here I am creating the math that will add all of the numbers together to get the sum. 
    }
    if(sum > 100){
      return true;      
    } 
   else                                  //created if/else statements so that if it is greater than 100 the call will return true and if less that 100 it will return false. 
{
    return false;
}
}
console.log(numbers(arr));      


//Write a function that takes an array of numbers and returns the average of all the elements in the array.//

function average(arr)  // I used the same numbers as the function above to work with in this segment of code. 
{
    sum=0;
    for(i=0; i<arr.length;i++)
    {                                                      //created a for loop to add the total number together reulting in 113. 
        sum += arr[i];
    }
    return(sum/arr.length);

}
console.log(sum/arr.length);    //printed to the console. 

//Write a function that takes two arrays of numbers and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.

let array1;
let array2;
function arrayAbove(array1, array2) {
    {
        for (let i = 0; i < array1; i++) { array1 = array1[i] / array1.length };
    } {                                                                                 //created a for loop for each array. 
        for (let i = 0; i < array2; i++) { array2 = array2[i] / array2.length };
        if (array1 > array2) { return true } else { return false };
    }
}
console.log(arrayAbove([1, 2, 3, 4], [1, 2, 3]));  //tried something different instead of creating the array at the top I printed them at the end at the bottom. 


//Write a function called willBuyDrink that takes a boolean isHotOutside, and a number moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.//
var isHotOutside = true;                 //created my variable for isHotOutSide and moneyInPocket
var moneyInPocket = 10.50;

function willBuyDrink(isHotOutside, moneyInPocket){       
    if (isHotOutside && moneyInPocket > 10.50) {    //Inside of my if statement I use the equality that will then print true or false based on the variables provided above. 
        return true;
    }
    else{
        return false;
    } 
}
var a=willBuyDrink(true, 12);
console.log(a);  


//Create a function of your own that solves a problem. In comments, write what the function does and why you created it. 
let rent = 1500; 
let paycheck = 3000;     //I created a function that will help someone with a budget to determine if they have enough money once rent is paid to go out this weekend.

function budget(rent, paycheck){    // Started with my function to check to see if the paycheck was more money than rent this month. 
    if(paycheck > rent) { return true; } 
    else { return false; }
 }
 console.log(budget(rent,paycheck,));

    const DIFFERENCE = (paycheck - rent); // Found the difference to see how much money we have left once rent is paid.
     console.log(DIFFERENCE);
    
    let bills = 700;             // I created a new variable to include the bills we have to pay this weekend as well. 
    
    if(DIFFERENCE - bills >= 500){     // I used an if statement to subtract the amount from what was left over after paying bils to determine if there is enough money left over to go out.
         console.log("I have enough money to go out this weekend!");
     } else  { 
         console.log("I do not have enough money to go out this weekend.");
     }
