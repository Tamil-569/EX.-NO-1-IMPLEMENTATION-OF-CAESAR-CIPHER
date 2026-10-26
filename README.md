# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char text[100];
    int key, i;

    printf("Enter a message: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter key: ");
    scanf("%d", &key);

    key = key % 26;

    for (i = 0; text[i] != '\0'; i++) {
        if (isupper(text[i])) {
            text[i] = (text[i] - 'A' + key) % 26 + 'A';
        }
        else if (islower(text[i])) {
            text[i] = (text[i] - 'a' + key) % 26 + 'a';
        }
    }

    printf("Encrypted message: %s", text);

    return 0;
}

```

## OUTPUT:
<img width="424" height="238" alt="{AFF4E25A-7659-4D35-88B0-C09D7F00568E}" src="https://github.com/user-attachments/assets/613e8877-cc6a-4218-b729-e18bbd971c72" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
