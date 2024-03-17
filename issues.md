So here I am planning to share views on some of the issues mentioned in the issues panel. 

## Mathsteps cannot handle quadratic equations #243

So for solving the quadratic equation there are lot of ways that we can do it like using the  
Quadratic Formula: x = [ -b (+-) sqrt(b^2 - 4ac) ] / 2a or like splitting the middle term. so I think with proper detailed algorithm we can add this cool feature. I will demonstarte a simple method using javascript two solve the quadratic equation.

function solveQuadratic(a, b, c) {
    let discriminant = b * b - 4 * a * c;

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

