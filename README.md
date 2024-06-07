# Lab 7

Lab 7 was an introduction to error handling, not only knowing how to catch one, but how to create them as well:
```ruby
class CustomError extends Error{
    constructor(args){
        super(args);
        this.name = "CustomError";
    }
}

throwGenericError = () => {
    console.log("Force generic error");
    try{
        console.log("Generic error try block");
        throw new Error("Generic error");
    } catch(error){
        console.log("Generic error catch block");
        console.log(`${error.name}: ${error.message}`)
    } finally{
        console.log("Generic error finally block");
    }
}

throwCustomError = () => {
    console.log("Force custom error");
    try{
        console.log("Custom error try block");
        throw new CustomError("Custom error");
    } catch(error){
        console.log("Custom error catch block");
        console.log(`${error.name}: ${error.message}`)
    } finally{
        console.log("Custom error finally block");
    }
}

throwGenericError();
throwCustomError();
```
<a href="https://joeybez.github.io/joeybezner.github.io/">Back to Home</a>
