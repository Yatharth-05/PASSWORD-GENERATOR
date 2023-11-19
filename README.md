# PASSWORD-GENERATOR

import random

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PYpass Generator")

let = int(input("How many letters do you want in your password?\n"))

num = int(input("How many numbers do you want in your password?\n"))

sym = int(input("How many symbols do you want in your password?\n"))

password = []

for char in range(1, let+1):
    password += random.choice(letters)

for char in range(1, num+1):
    password += random.choice(numbers)

for char in range(1, sym+1):
    password += random.choice(symbols)


random.shuffle(password)


finalpassword = ""
for char in password:
    finalpassword += char

print("Your password is : " + finalpassword)
