## Lab 7

<img width="1083" alt="lab-07" src="https://user-images.githubusercontent.com/84175061/120881759-50fe4f80-c588-11eb-8a54-924f6c63565b.png">


### lab-07.js
```
/*
Name: Brianna Wei
CIT 281
Lab-07.js
*/

class CustomError extends Error {
    constructor(args) {
        super(args);
        this.message = "Custom Error"
    }

    throwGenericError() {
        throw new Error("Generic Error");
    }

    throwCustomError() {
        throw new CustomError().message;
    }
}

const myError = new CustomError();

console.log("Force Generic Error");


try {
    // try block
    console.log("Generic Error Try Block");
    myError.throwGenericError();
} catch {
    console.log("Generic Error Catch Block");
    console.log(myError.throwGenericError());
} finally {
    console.log("Generic Error Finally Block")
}



console.log("Force Custom Error");

try {
    console.log("Custom Error Try Block");
    myError.throwGenericError();
} catch {
    console.log("Custom Error Catch Block");
    console.log(myError.throwCustomError());
} finally {
    console.log("Custom Error Finally Block")
}

```
