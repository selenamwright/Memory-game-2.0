# Memory-game-2.0
import random

cards = [1, 1, 2, 2, 3, 3]
random.shuffle(cards)

picked_cards = []
while len(picked_cards) < len(cards):
    print("Current board: ", ["X" if i not in picked_cards else str(cards[i]) for i in range(len(cards))])
    try:
        input1 = int(input("Pick a card by its index: "))
        input2 = int(input("Pick another card by its index: "))
        if input1 not in picked_cards and input2 not in picked_cards:
            if cards[input1] == cards[input2]:
                picked_cards.append(input1)
                picked_cards.append(input2)
                print("You found a match!")
            else:
                print("Sorry, try again.")
        else:
            print("You have already picked that card. Try again.")
    except ValueError:
        print("Invalid input. Please enter a number.")

print("Congratulations, you found all the matches!")
