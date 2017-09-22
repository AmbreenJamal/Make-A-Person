<h2>DNA Pairing</h2>
  
<p>getFirstName()  
getLastName()  
getFullName()  
setFirstName(first)  
setLastName(last)  
setFullName(firstAndLast)</p>  
<p>Run the tests to see the expected output for each method.  
  
The methods that take an argument must accept only one argument and it has to be a string.  
 
These methods must be the only available means of interacting with the object.</p>  
  
<ul>
<li>Object.keys(bob).length should return 6.</li>
<li>bob instanceof Person should return true.</li>
<li>bob.firstName should return undefined.</li>
<li>bob.lastName should return undefined.</li>
<li>bob.getFirstName() should return "Bob".</li>
<li>bob.getLastName() should return "Ross".</li>
<li>bob.getFullName() should return "Bob Ross".</li>
<li>bob.getFullName() should return "Haskell Ross" after bob.setFirstName("Haskell").</li>
<li>bob.getFullName() should return "Haskell Curry" after bob.setLastName("Curry").</li>
<li>bob.getFullName() should return "Haskell Curry" after bob.setFullName("Haskell Curry").</li>
<li>bob.getFirstName() should return "Haskell" after bob.setFullName("Haskell Curry").</li>
<li>bob.getLastName() should return "Curry" after bob.setFullName("Haskell Curry").</li>
</ul>
</p><br/>
<p>======================================================</p>
  
var Person = function(firstAndLast) {  
    // Complete the method below and implement the others similarly   
        
    var arr = firstAndLast.split(" "); 
    fname=arr[0];  
    lname=arr[1];  
   this.getFullName = function(firstAndLast) {  
 
     return fname+" "+lname;  
       
    };  
  this.getFirstName=function()  
  {  
     return fname;  
  };  
  this.getLastName=function()  
  {  
     return lname;  
  };  
  this.setFirstName= function(first)  
  {  
    fname= first;  
  };  
  this.setLastName= function(last)  
  {  
    lname= last;  
  };  
  this.setFullName =function(firstAndLast)  
  {  
    var arr1 = firstAndLast.split(" ");   
     fname=arr1[0];  
     lname=arr1[1];  
    return  fname+" "+lname;  
  };    
};  
  
var bob = new Person("Bob Ross");  
  
bob.getFullName();  
bob.getFullName();  