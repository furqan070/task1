import random
import string

def generate_password(length, use_uppercase, use_digits, use_special_chars):
    # Define the character sets based on user preferences
    characters = string.ascii_lowercase  # Always include lowercase letters

    if use_uppercase:
        characters += string.ascii_uppercase
    if use_digits:
        characters += string.digits
    if use_special_chars:
        characters += "!@#$%^&*()-_=+[]{}|;:',.<>?/~`"
    
    # Ensure that the characters set is not empty
    if not characters:
        raise ValueError("No character types selected for password generation.")
    
    # Generate the password
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    # User input for password length
    while True:
        try:
            length = int(input("Enter the desired password length: "))
            if length <= 0:
                raise ValueError("Length must be a positive integer.")
            break
        except ValueError as e:
            print(f"Invalid input: {e}. Please enter a positive integer.")

    # User input for password complexity
    use_uppercase = input("Include uppercase letters? (yes/no): ").strip().lower() == 'yes'
    use_digits = input("Include digits? (yes/no): ").strip().lower() == 'yes'
    use_special_chars = input("Include special characters? (yes/no): ").strip().lower() == 'yes'

    # Generate and display the password
    password = generate_password(length, use_uppercase, use_digits, use_special_chars)
    print("Generated password:", password)

if _name_ == "_main_":
    main()
