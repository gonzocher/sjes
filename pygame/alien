# Ex 07 Add score

# Click on alien (sounds don't work on replit)
# Try # on screen.clear() or change alien.topright numbers
import pgzrun

alien = Actor('alien')
alien.topright = 0, 10

WIDTH = 500
HEIGHT = alien.height + 20

# Add title
TITLE = "Alien Invasion"

# Add icon
ICON = 'images/alien.png'

# Declare variables
attempts = 0
score = 0

# Talk with the player
print("\n\nAliens have invaded earth!\n")
name = input("What's your name?\n\n")
print("\nWelcome, " + name + ", we hope you have come to rescue us! Click on the alien")

# Draw the screen
def draw():
    screen.clear()
    screen.fill((0, 128, 0))
    alien.draw()

# Start the alien moving
def update():
    alien.left += 2
    if alien.left > WIDTH:
        alien.right = 0     

# If click alien
def on_mouse_down(pos):
    if alien.collidepoint(pos):
        set_alien_hurt()
        global score 
        score += 1
        global attempts
        attempts += 1
        print(f"Your score is: {score}, in {attempts} attempts.")
    else:
        attempts += 1    
        print("You missed me!")

# When clicked
def set_alien_hurt():
    alien.image = 'alien_hurt'
    #sounds.eep.play()
    clock.schedule_unique(set_alien_normal, 1.0)

# Return to normal alien
def set_alien_normal():
    alien.image = 'alien'

pgzrun.go()    
