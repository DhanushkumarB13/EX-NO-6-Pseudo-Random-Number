# Exp NO-6-Pseudo-Random-Number

```
NAME: B.DHANUSH KUMAR
REG NO: 212224240034
```

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
Start the program and import the required libraries.
Seed the random number generator using the current time(i.e) rand(time(0));
Get the number of randon number to generate.
Pass the value for number of iterations and print the numbers.
End the program.

# PROGRAM:

#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296U  // This is not used in the calculation but kept for reference

unsigned int lcg(unsigned int seed) {
    return A * seed + C;  // Modulo 2^32 is implicit with unsigned int overflow
}

int main() {
    unsigned int seed;
    int n;

    printf("Enter the seed value: ");
    scanf("%u", &seed);

    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);

    printf("Random numbers:\n");
    for (int i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }

    return 0;
}

# OUTPUT:

![Screenshot 2025-04-23 181629](https://github.com/user-attachments/assets/855a4d68-d162-4825-947b-26c1bce3865f)

# RESULT:

Implemented Pseudorandom Number Generation Using Standard library successfully.
