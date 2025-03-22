import pygame

# Initialize Pygame
pygame.init()

# Set up display
WIDTH, HEIGHT = 600, 400
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Pygame Polygon Example")

# Define colors
WHITE = (255, 255, 255)
BLUE = (0, 0, 255)

#  polygon points
points = [(100, 300), (200, 200), (300, 300), (250, 350), (150, 350)]

# Main loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    
    # Fill background
    screen.fill(WHITE)
    
    # Draw polygon
    pygame.draw.polygon(screen, BLUE, points)
    
    # Update display
    pygame.display.flip()

# Quit Pygame
pygame.quit()
