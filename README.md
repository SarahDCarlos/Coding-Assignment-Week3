"# Coding-Assignment-Week3" 

//Create an array called ages that contains the following values: 3, 9, 23, 64, 2, 8, 28, 93.//
//Programmatically subtract the value of the first element in the array from the value in the last element of the array (do not use numbers to reference the last element, find it programmatically, ages[7] – ages[0] is not allowed). Print the result to the console.//

var ages = [3, 9, 23, 64, 2, 8, 28, 93]  //array I created 
ages.push(20)                            //pushed an additional number
var sum= 0, avg = 0.0                     //Created a for loop that will add the numbers together to get a toal of 250. 
for(var i=0; i < ages.length; i++){
    sum = sum + ages[i] 
    console.log(sum); 
}
avg = sum / ages.length         //Using ages.length to find the average of the number of letters found in the array. 
console.log(avg)

var last = ages[ages.length - 1] 
var first = ages[ages.length - ages.length] 
diff = last - first 

console.log(`Difference between first and last element is: ${diff}`)



//Create an array called names that contains the following values: ‘Sam’, ‘Tommy’, ‘Tim’, ‘Sally’, ‘Buck’, ‘Bob’.//

//Use a loop to iterate through the array and calculate the average number of letters per name. Print the result to the console.//
//Use a loop to iterate through the array again and concatenate all the names //

var names = [' Sam ', ' Tommy ', ' Tim ', ' Sally ', ' Buck ', ' Bob '];     
sum=0;
for(i=0; i < names.length; i++){                                //created a for loop that will add all the letters together and divide it to get the average. 
    sum=sum + names[i].length;
}console.log('Letters per name:',sum/names.length);

//part 2b 
console.log(names.join(" "));   // This line of code will join all of the names together


//you can access the last element of an array using 
//you can access the first element of an array using

//Write a function that takes two parameters, word and n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in ‘Hello’ and 3, I would expect the function to return ‘HelloHelloHello’).//
function concat_n_time(word,n)
{
var con= word;
for (i=1; i<=n; i++)        //for loop that will take my words incrementing up.
{
    con= con.concat(word);
}
return con;
}
console.log(concat_n_time("Hello",2));   //Used this line to print it to the console to get the Hello result three times. 



//Write a function that takes two parameters, firstName and lastName, and returns a full name (the full name should be the first and the last name separated by a space).//
function fullName(firstName, lastName){               // created a function with first name and last name as parameters. 
    console.log(firstName + " " + lastName);           // Created a space between my first and last name. 
}
fullName('Sarah', 'Carlos')



//Write a function that takes an array of numbers and returns true if the sum of all the numbers in the array is greater than 100.//
var arr= [5, 8, 10, 40, 35, 15]

function numbers(arr){                       
    sum = 0;                                
    for(i=0; i<arr.length; i++)          
    {                                   //used a sum=0 so that when I do the math on line 69 there is a starting point and something to add. 
        sum=sum+arr[i];
    }

    if(sum > 100)                       //Created an if statement to check to see if the sum of all the numbers is greater than 100. 
    {
      return true;
    } 
   else
{
    return false;
}

}
console.log(numbers(arr));


//Write a function that takes an array of numbers and returns the average of all the elements in the array.//

function average(arr)               
{
    sum=0;
    for(i=0; i<arr.length;i++)
    {
        sum=sum+arr[i];         // This line adds all of the numbers together.
    }
    return(sum/arr.length);     //This line divided the added number by the amount of numbers to get the average. 
}

console.log(average(arr));      //printed it to the console to get the average. 

//Write a function that takes two arrays of numbers and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.

let array1;
let array2;                                                                             
function arrayAbove(array1, array2) {
    {
        for (let i = 0; i < array1; i++) { array1 = array1[i] / array1.length };     //created a for loop for each array that will find the average of each array. 
    } {
        for (let i = 0; i < array2; i++) { array2 = array2[i] / array2.length };      
        if (array1 > array2) { return true } else { return false };
    }
}
console.log(arrayAbove([1, 2, 3, 4], [1, 2, 3]));       //Here I attempted to do the arrays a different way. Instead of adding the numbers in the array in line 101 and 102 I added it by console logging the numbers at the end to the array.



//Write a function called willBuyDrink that takes a boolean isHotOutside, and a number moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.//
var isHotOutside = true;                                            
var moneyInPocket = 10.50;

function willBuyDrink(isHotOutside, moneyInPocket){
    if (isHotOutside && moneyInPocket > 10.50) {    //used if/else sttement to return true or false based on the condition. 
        return true;
    }
    else{
        return false;
    } 
}
console.log(willBuyDrink);

//Create a function of your own that solves a problem. In comments, write what the function does and why you created it.
let rent = 1500;
let paycheck = 3000;                                                        //I created a function that will help someone with a budget to determine if they have enough money once rent is paid to go out this weekend. 

function budget(rent, paycheck){                                        // Started with my function to check to see if the paycheck was more money than rent this month. 
    if(paycheck > rent) { return true; }
    else { return false; }
}
console.log(budget(rent,paycheck,));

const DIFFERENCE = (paycheck - rent);                                   // Found the difference to see how much money we have left once rent is paid. 
console.log(DIFFERENCE);

let bills = 700;                                                        // I created a new variable to include the bills we have to pay this weekend as well. 
if(DIFFERENCE - bills >= 500){                                          // I used an if statement to subtract the amount from what was left over after paying bils to determine if there is enough money left over to go out. 
    console.log("I have enough money to go out this weekend!");
} else {
    console.log("I do not have enough money to go out this weekend.");
}

