# Ex-10---Diffie-Hellman-Key-Exchange-Algorithm
## AIM:
	To implement key exchange between users using Diffie Hellman algorithm.

## ALGORITHM:
•	Get the input for prime number p. 

•	Calculate the primitive root of p that is g.

•	Calculate private keys for both users using p and g values.

•	Similarly, secret keys for both users are calculated.

## PROGRAM:
```
#include <math.h>
#include <stdio.h>

// Power function to return value of a^b mod P
long long int power(long long int a, long long int b, long long int P) {
    if (b == 1)
        return a % P;
    else
        return (((long long int)pow(a, b)) % P);
}

int main() {
    long long int P, G, x, a, y, b, ka, kb;

    printf("\n***** Diffie-Hellman Key Exchange Algorithm *****\n\n");

    // Input public keys P and G
    printf("Enter the value of P (a prime number): ");
    scanf("%lld", &P);
    printf("The value of P: %lld\n", P);

    printf("Enter the value of G (Primitive root of P): ");
    scanf("%lld", &G);
    printf("The value of G: %lld\n\n", G);

    // Alice's private key
    a = 4;
    printf("The private key a for Alice: %lld\n", a);
    x = power(G, a, P);
    
    // Bob's private key
    b = 3;
    printf("The private key b for Bob: %lld\n", b);
    y = power(G, b, P);

    // Generating the secret keys
    ka = power(y, a, P); // Secret key for Alice
    kb = power(x, b, P); // Secret key for Bob

    // Display results
    printf("\nSecret key for Alice is: %lld\n", ka);
    printf("Secret key for Bob is: %lld\n", kb);

    return 0;
}

```

## OUTPUT:
![Screenshot 2024-11-18 101016](https://github.com/user-attachments/assets/8db2cebf-c51b-45c9-8fbf-c0190d48e175)

## RESULT:
	Hence, the simulation of Diffie Hellman algorithm is successfully done.

