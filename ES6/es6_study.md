# ES6 self study 

### Generators

* To define an iterative algorithm by writing a single function which can **MAINTAIN its own STATE**.
* works as a FACTORY for iterators. 
* When it is executed it returns a **NEW** Generator object. 

> Basic Syntax
>
> function* function_name(){ }
> 

* Used with **yield** and loop
  
  * yield pauses generator functions and returns the value of [expression] to caller.
  
 ```
 function* function_name(){
    while(true) {
      [rv] = yield [expression];
     }
 }
```
 

> 
 
 * Example

```javascript

[ Source Code ]

function* idMaker() {
  var index = 0;
  var str = 'The former indexes '
  while(true){
    index++;
    yield str += ' ' + index; //yield : to pause and resume a generator function
  }
    
}

console.log( '------ Genertator : function* -------')

var gen = idMaker();

console.log( '[gen]' + gen.index + '[str]' + gen.str); //shown as undefined 
console.log('next,' + gen.next().value); //index: 1
gen.next(); //index: 2
console.log('next');
console.log('next,' + gen.next().value); //index: 3
console.log('next,' + gen.next().value); //index: 4
gen.next(); //index: 5
console.log('next');
console.log('next,' + gen.next().value); //index: 6
console.log('[gen]' + gen.index + '[str]' + gen.str); //shown as undefined 

[ Output ]
------ show function* ------- 
[gen]undefined[str]undefined 
next,The former indexes  1 
next 
next,The former indexes  1 2 3 
next,The former indexes  1 2 3 4 
next 
next,The former indexes  1 2 3 4 5 6 
[gen]undefined[str]undefined 
```