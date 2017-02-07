Define a closure: 
         A closure is the inner function which can access with local variables defined for a parent function even after the parent function 
 has returned.
 
 In simple Words:
 JavaScript variables are  belong to the local or global scope.
  Local space is that define inside a function.
   Global variables can be made local (private) with closures.
 
 Example of Local scope(Variables):
      A function can access all variables which are defined inside this function.
      
      function add() {
    var a = 2;
    return a + a;
} 
 Output is 2+2=4
     This a is a local variable.
     
Example of Global Scope(Variable):
      A Variable which is outside the fuction and the function can even access it, is called global variable.
      
      var a = 4;
function myFunction() {
    return a * a;
} 
  Output is 4*4=16
  This is Global Variable.
  
  Now,Example of closure:
  How the inner function can become the closure and can  access the parent variables.
   A closure is formed when one of those inner functions is made accessible outside of the function in which it was contained,
 so that it may be executed after the outer function has returned.

       
      var a = 4;
function myFunction() 
{ var b =2;
   function add()
   {
        var sum=0;
        return sum=a+b;
    }

return sum;    
} 

myFunction();

In the above example, the inner function add() will be able to access the global variale a and variable b defined in the funcion
and will return the value of sum. But the return sum in the function myFunction will not work  as the inner function is a closure 
and the outer function will not be able to access the inner function's variable sum. The reason being sum is defined locally inside
the add() function so it limit its scope and hides it from the outer function i.e myFunction.
  
    




