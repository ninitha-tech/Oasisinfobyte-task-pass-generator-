# Oasisinfobyte-task-password-generator-
import random

letters = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"
numbers = "0123456789"
symbols = "!@#$%^&*"

password = ""

length = int(input("Enter password length: "))

use_letters = input("Include letters? (y/n): ")
use_numbers = input("Include numbers? (y/n): ")
use_symbols = input("Include symbols? (y/n): ")

characters = ""

if use_letters == "y":
    characters = characters + letters

if use_numbers == "y":
    characters = characters + numbers

if use_symbols == "y":
    characters = characters + symbols

for i in range(length):
    password = password + random.choice(characters)

print("Generated Password:", password)
