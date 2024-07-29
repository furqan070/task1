import random

def play_round():
    choices = ['rock', 'paper', 'scissors']
    computer_choice = random.choice(choices)
    user_choice = input("Enter your choice (rock/paper/scissors): ").lower()

    if user_choice in choices:
        print("Computer's choice:", computer_choice)
        if user_choice == computer_choice:
            print("It's a tie!")
            return 'tie'
        elif (user_choice == 'rock' and computer_choice == 'scissors') or \
             (user_choice == 'scissors' and computer_choice == 'paper') or \
             (user_choice == 'paper' and computer_choice == 'rock'):
            print("You win!")
            return 'user'
        else:
            print("Computer wins!")
            return 'computer'
    else:
        print("Invalid choice! Please enter rock, paper, or scissors.")
        return 'invalid'

def main():
    rounds = int(input("Enter the number of rounds you want to play: "))
    user_score = 0
    computer_score = 0
    
    for round_num in range(1, rounds + 1):
        print(f"Round {round_num}:")
        result = play_round()
        if result == 'user':
            user_score += 1
        elif result == 'computer':
            computer_score += 1

        print(f"User Score: {user_score}, Computer Score: {computer_score}")

    print("Game over!")
    if user_score > computer_score:
        print("Congratulations! You win the game!")
    elif user_score < computer_score:
        print("Sorry! Computer wins the game!")
    else:
        print("It's a tie!")

if _name_ == "_main_":
    main()
