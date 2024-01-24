import time
import random

def introduction():
    print("You find yourself alone in a dark, abandoned mansion. Strange sounds echo through the halls.")
    print("Your goal is to survive the night and uncover the mysteries within. Be careful with your choices.")

def make_choice():
    print("1. Enter the creepy hallway.")
    print("2. Investigate the mysterious noise.")
    print("3. Try to find a way out.")

    choice = input("Enter your choice (1, 2, or 3): ")
    return choice

def creepy_hallway():
    print("As you enter the hallway, you hear creaking footsteps behind you.")
    print("1. Turn around to see what it is.")
    print("2. Keep walking forward.")

    choice = input("Enter your choice (1 or 2): ")
    return choice

def mysterious_noise():
    print("You approach the source of the noise and find an old, dusty piano playing by itself.")
    print("1. Investigate the piano.")
    print("2. Leave the room immediately.")

    choice = input("Enter your choice (1 or 2): ")
    return choice

def find_a_way_out():
    print("You search for an exit but find a locked door.")
    print("1. Look for a key.")
    print("2. Attempt to break the door down.")

    choice = input("Enter your choice (1 or 2): ")
    return choice

def main():
    introduction()

    while True:
        choice = make_choice()

        if choice == "1":
            choice = creepy_hallway()
            if choice == "1":
                print("A shadowy figure emerges, and you feel a cold hand on your shoulder.")
                print("You have been captured. Game over.")
                break
            elif choice == "2":
                print("You continue down the hallway cautiously.")
                # Add more scenarios or encounters based on choices.

        elif choice == "2":
            choice = mysterious_noise()
            if choice == "1":
                print("The piano suddenly stops playing, and the room falls silent.")
                # Add more scenarios or encounters based on choices.
            elif choice == "2":
                print("You rush out of the room, heart pounding.")
                # Add more scenarios or encounters based on choices.

        elif choice == "3":
            choice = find_a_way_out()
            if choice == "1":
                print("You find a rusty key on a dusty shelf.")
                # Add more scenarios or encounters based on choices.
            elif choice == "2":
                print("Your attempts to break the door down attract unwanted attention.")
                print("You have been caught. Game over.")
                break

# Run the game
if __name__ == "__main__":
    main()
