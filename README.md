# TASK-3-PASSWORD-GENERATOR-
import random
import string

def generate_password(length):
    # Define the character sets to include in the password
    characters = string.ascii_letters + string.digits + string.punctuation
    
    # Generate a random password
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    print("Password Generator")
    try:
        # Prompt the user for password length
        length = int(input("Enter the desired length of the password: "))
        
        if length < 4:
            print("Password length should be at least 4 characters for better security.")
        else:
            # Generate and display the password
            password = generate_password(length)
            print("Generated Password:", password)
    except ValueError:
        print("Please enter a valid number for the length.")

# Run the password generator
main()



output 

Password Generator
Enter the desired length of the password: 12
Generated Password: A7f$k!8#P1cQ
