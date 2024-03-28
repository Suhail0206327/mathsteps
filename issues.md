So here I am planning to share views on some of the issues mentioned in the issues panel. 

## Mathsteps cannot handle quadratic equations #243

So for solving the quadratic equation there are lot of ways that we can do it like using the  
Quadratic Formula: x = [ -b (+-) sqrt(b^2 - 4ac) ] / 2a or like splitting the middle term. so I think with proper detailed algorithm we can add this cool feature. I will demonstarte a simple method using javascript two solve the quadratic equation.

function solveQuadratic(a, b, c) {
    let discriminant = (b * b) - (4 * a * c);
    if (discriminant < 0) {
        return "No real roots";
    } else if (discriminant === 0) {
        return -b / (2 * a);
    } else {
        let root1 = (-b + Math.sqrt(discriminant)) / (2 * a);
        let root2 = (-b - Math.sqrt(discriminant)) / (2 * a);
        return [root1, root2];
    }
}

### I will break down the above function to simple steps:

1. First are creating a function which can take three parameters a, b, c. In a basic quadratic equation ax + bx^2 + c. a is the coefficient of x, b is the coefficient of x^2 and c is the constant. 

2. Now we are creating new variable  discriminant. The will calculate the value of (b * b) - (4 * a * c). 

The number of roots (the solutions) depends on the discriminant that I mentioned here. if value is negative it won't be having any real roots (maybe in the complex plane). if the value is zero then there is only one root and if it is positive then there will be two roots (coming from the +/- in the quadratic formula).

3. Using an if statement to check the above statements. 

Here if the discriminant is less than zero  it is returning a message showing that, if zero its returining the value of the single root. Other wise in the else statement its calculating the two roots using he sqrt method from the math class. Square root is basically the exponential power 1/2. 
