# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
Start the program and import the required libraries.
Seed the random number generator using the current time(i.e) rand(time(0));
Get the number of randon number to generate.
Pass the value for number of iterations and print the numbers.
End the program.

# PROGRAM:
```
Name: R sheetal
Reg No: 212223230206
```

```
#include <stdio.h>

#define A 1664525
#define C 1013904223

unsigned int lcg(unsigned int seed) {
    return A * seed + C; // No need for % 2^32; it wraps around naturally
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
```
# OUTPUT:
![Screenshot 2025-05-15 083053](https://github.com/user-attachments/assets/56672e81-207a-4195-9e58-0d89be44184c)

# RESULT:
The Program is implemented successfully.
