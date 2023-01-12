# Memory-game-2.0
pip install pygame
import random

# Initialize Pygame
pygame.init()

# Window size and caption
size = (500, 700)
screen = pygame.display.set_mode(size)
pygame.display.set_caption("Memory Game")

# Load card images
card_images = [pygame.image.load("import pygame
import random

# Initialize Pygame
pygame.init()

# Set window size and caption
size = (500, 700)
screen = pygame.display.set_mode(size)
pygame.display.set_caption("Memory Game")

# Load card images
card_images = []

# Create a list of cards
cards = []
for i in range(5):
    cards.append(i)
    cards.append(i)
random.shuffle(cards)

# List to store the cards that have been flipped
flipped_cards = []

# List to store the cards that have been matched
matched_cards = []

# Initialize variables for the game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Draw background
    screen.fill((255, 255, 255))

    # Draw cards
    for i in range(len(cards)):
        x = 50 + i * 100
        y = 200
        if i in flipped_cards:
            screen.blit(card_images[cards[i]], (x, y))
        else:
            pygame.draw.rect(screen, (0, 0, 255), (x, y, 75, 100))

    # Mouse clicks
    if pygame.mouse.get_pressed()[0]:
        pos = pygame.mouse.get_pos()
        for i in range(len(cards)):
            x = 50 + i * 100
            y = 200
            if x < pos[0] < x + 75 and y < pos[1] < y + 100:
                if i not in flipped_cards and i not in matched_cards:
                    flipped_cards.append(i)
                    if len(flipped_cards) == 2:
                        if cards[flipped_cards[0]] == cards[flipped_cards[1]]:
                            matched_cards.append(flipped_cards[0])
                            matched_cards.append(flipped_cards[1])
                            flipped_cards = []
                            if len(matched_cards) == len(cards):
                                print("Congratulations, you found all the matches!")
                        else:
                            flipped_cards = []
    pygame.display.update()

# Exit Pygame
pygame.quit()), 

# List of cards
cards = []
for i in range(5):
    cards.append(i)
    cards.append(i)
random.shuffle(cards)

# Create a list to store the cards that have been flipped
flipped_cards = []

# Create a list to store the cards that have been matched
matched_cards = []

# Initialize variables for the game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Draw background
    screen.fill((255, 255, 255))

    # Draw cards
    for i in range(len(cards)):
        x = 50 + i * 100
        y = 200
        if i in flipped_cards:
            screen.blit(card_images[cards[i]], (x, y))
        else:
            pygame.draw.rect(screen, (0, 0, 255), (x, y, 75, 100))

    # Mouse clicks
    if pygame.mouse.get_pressed()[0]:
        pos = pygame.mouse.get_pos()
        for i in range(len(cards)):
            x = 50 + i * 100
            y = 200
            if x < pos[0] < x + 75 and y < pos[1] < y + 100:
                if i not in flipped_cards and i not in matched_cards:
                    flipped_cards.append(i)
                    if len(flipped_cards) == 2:
                        if cards[flipped_cards[0]] == cards[flipped_cards[1]]:
                            matched_cards.append(flipped_cards[0])
                            matched_cards.append(flipped_cards[1])
                            flipped_cards = []
                            if len(matched_cards) == len(cards):
                                print("Congratulations, you found all the matches!")
                        else:
                            flipped_cards = []
    pygame.display.update()

# Exit Pygame
pygame.quit()
