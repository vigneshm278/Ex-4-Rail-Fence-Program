# Ex--5-Rail-Fence-Program

# IMPLEMENTATION OF RAIL FENCE – ROW & COLUMN TRANSFORMATION TECHNIQUE

# AIM:

# To write a C program to implement the rail fence transposition technique.

# DESCRIPTION:

In the rail fence cipher, the plain text is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

# ALGORITHM:

STEP-1: Read the Plain text.
STEP-2: Arrange the plain text in row columnar matrix format.
STEP-3: Now read the keyword depending on the number of columns of the plain text.
STEP-4: Arrange the characters of the keyword in sorted order and the corresponding columns of the plain text.
STEP-5: Read the characters row wise or column wise in the former order to get the cipher text.

# PROGRAM :
```
text = input("Enter a Secret Message:\n")
rails = int(input("Enter number of rails:\n"))

fence = ['' for _ in range(rails)]
rail = 0
dir = 1

for char in text:
    fence[rail] += char
    if rail == 0:
        dir = 1
    elif rail == rails - 1:
        dir = -1
    rail += dir

print("Encrypted Message:")
print(''.join(fence))
```
# OUTPUT :

![Screenshot 2025-04-22 183124](https://github.com/user-attachments/assets/7e7f925a-1004-4771-921b-3a1d3b4e2d68)


# RESULT :

 The program is executed successfully.
