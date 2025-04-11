2-3)The first call returns undefined because the function is called without the object, so this loses its connection.
The second call works because it's called on the object, so this correctly refers to it and returns the full name.
4)Inside catch, x is block-scoped because of catch(x) and assigned 1, so it prints 1.
Outside catch, x is not defined (block scope), so it prints undefined.
Variable y is declared with var (function-scoped), so it exists outside catch and prints 2.
5)Inside inner(), var b is hoisted as undefined.
b++ means undefined + 1 → gives NaN.
Then b = 3 → prints 3.
6)library.sort(function(a, b) {
  return a.title.localeCompare(b.title);
});
console.log(library);
7)function alphabetOrder(str) {
  return str.split('').sort().join('');
}
console.log(alphabetOrder("welcome"));
1-3)Even though we used three arrays, arr1 and arr2 end up being the same object due to .reverse(). Then we push arr3 as a single element, which makes the last element of arr1 and arr2 an array. When printing, JavaScript converts that inner array into a string.
4)The first call returns undefined because the function is called separately, so this does not refer to the original object. It loses its context.
The second call returns "John Doe" because the method is called directly on the object, so this correctly refers to the object and accesses its _name property.
5)Even though x is declared as 21 outside the function, inside the function x is declared again using var, which gets hoisted to the top of the function without its value.
So when console.log(x) runs, it's referring to the local x, which exists but is still undefined at that point.
The value 20 is assigned after the console.log.
That’s why the output is undefined.
6)function uniqueChars(str) {
  let result = "";
  for (let i = 0; i < str.length; i++) {
    if (result.indexOf(str[i]) === -1) {
      result += str[i];
    }
  }
  return result;
}
7)function uniqueChars(str) {
  let result = "";
  for (let i = 0; i < str.length; i++) {
    if (result.indexOf(str[i]) === -1) {
      result += str[i];
    }
  }
  return result;
}
1. Difference between Cookie-based and JWT Token-based Authentication :session data on the server and uses a browser cookie (usually with a session ID) to identify users. The server must keep track of all sessions.all user info in a self-contained token (JSON Web Token) on the client side. The token is sent with each request and verified by the server without storing session data.
2. Difference between Prototypal and Classical Inheritance :	Prototypal Inheritance: Objects inherit directly from other objects. It’s flexible and dynamic, used commonly in JavaScript (Object.create()).and instances. Objects are instances of classes, and inheritance is defined at class level (used in languages like Java, C++).
1. Describe Closure in JavaScript :
A closure is when a function “remembers” and has access to variables from its outer scope, even after the outer function has finished executing.
2.What is an HttpOnly Cookie? :
An HttpOnly cookie is a type of cookie that cannot be accessed via JavaScript (e.g., document.cookie). It can only be sent in HTTP requests.
This improves security by helping to prevent cross-site scripting (XSS) attacks.

