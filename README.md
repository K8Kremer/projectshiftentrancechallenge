# projectshiftentrancechallenge

//start problem 1
function cityBrag() {
  alert ("Durham is awesome!");
  }

//start problem 2
const bands = ['Kiss', 'Aerosmith', 'ACDC', 'Led Zeppelin', 'Nickelback'];
for (var i = 0; i < bands.length; i++){
alert ("I love " + bands[i] + ".");
  }
  
  // start problem 3
 const bands = ['Kiss', 'Aerosmith', 'ACDC', 'Led Zeppelin', 'Nickelback'];
 for (var i = 0; i < bands.length; i++){
    if (i < bands.length-1){
      console.log ("I love " + bands[i] + ".");
      }
  else {
    console.log ("I DON'T love " + bands[i] + ".")
   }
  }
  
  //start problem 4
const array = [34, 203, 16, 46, 34, 432, 342, 124, 33, 188, 12];
var avg = array => array.reduce((totalValue, currentValue) => totalValue + currentValue,0)/array.length;
console.log(avg(array));


  //start problem 5 which I have made more complicated than it needed to be
const array = ['a', 'b', 'c', 'd', 'c', 'b', 'b', 'c', 'a', 'e', 'b', 'e'];

function findMostFrequent(array){
  var arrayMap = array.reduce(function(lastValue, currValue){
    lastValue[currValue] = ++lastValue[currValue] || 1;
    return lastValue;
 //use reduce to increment element count while iterating through array
  },{});
  
  var mostFrequent = Object.keys(arrayMap)[0];
  for (var key in arrayMap){
       mostFrequent = arrayMap[mostFrequent]< arrayMap[key] ? key : mostFrequent;
       }
  return mostFrequent;
  }
 //access object properties to identify most frequent element in arrayMap
  console.log("The most frequent element is: " + findMostFrequent(array) + ".");

function findLeastFrequent(array){
  var arrayMap = array.reduce(function(lastValue, currValue){
    lastValue[currValue] = ++lastValue[currValue] || 1;
    return lastValue;
  },{});
 
  var leastFrequent = Object.keys(arrayMap)[0];
  for (var key in arrayMap){
    leastFrequent = arrayMap[leastFrequent] > arrayMap[key] ? key : leastFrequent;
    }
  return leastFrequent;
}
console.log ("The least frequent element is: " + findLeastFrequent(array)+ ".");


//start Problem 6; did not accomplish goal

const firstArray = ['a', 'b', 'c', 'a', 'a', 'b', 'd'];
const secondArray = ['a', 'b', 'b', 'a', 'e', 'c', 'c', 'g'];

var newArray=[];
for (var i = 0; i<secondArray.length; i++){
    if (firstArray.includes(secondArray[i]))
      var overlap = newArray.push(secondArray[i]);
    }
console.log(newArray);


//Problem 7:
function BillDisplay (hundreds, twenties, fives){
  this.hundreds = hundreds;
  this.twenties = twenties;
  this.fives = fives;
}
function makeChange(cost){
  var hundreds = parseInt(cost/100);
  var twenties = parseInt((cost-(hundreds*100))/20);
  var fives = parseInt((cost - (hundreds*100)-(twenties*20))/5);
  var newCost = new BillDisplay (hundreds,twenties,fives);
  return newCost;
                           
}
console.log(makeChange(1745));







