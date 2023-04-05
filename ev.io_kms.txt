import pyautogui
import time
import keyboard
import random

# 1373, 103


# Wavit for 1 second before startingv
pyautogui.sleep(1)


# Hold down the "w" key until program is terminated
pyautogui.keyDown('w')

def main_func():
    random_num = random.randint(1,4)
    pyautogui.click()
    pyautogui.sleep(0.1)

    # Get the current position of the mouse
    x, y = pyautogui.position()

    # Calculate the new x-coordinate for the mouse



    # Move the mouse smoothly to the new position


    # Generate a random direction (left or right)
    direction = random.choice(['left', 'right'])

    # Move the mouse horizontally by 50 pixels in the random direction
    if direction == 'left':
        random_x = random.randint(900, 1280)
        new_x = 1280 - random_x
        pyautogui.dragTo(new_x, y, duration=0.17)
        print("drag left " + "-"+str(random_x))
        pyautogui.sleep(0.5)
    else:
        random_x2 = random.randint(900, 1270)
        new_x_right = 1280 + random_x2
        pyautogui.dragTo(new_x_right, y, duration=0.17)
        print("drag right " + str(random_x2))
        pyautogui.sleep(0.5)

    pyautogui.sleep(0.3)
    pyautogui.keyDown('v')
    pyautogui.keyUp('v')
    pyautogui.keyDown('w')
    pyautogui.sleep(2.5)


    # if random == 1:
    #     pyautogui.keyDown('t')
    #     pyautogui.keyUp('t')
    #     print("land mine")
    # elif random == 2:
    #     pyautogui.scroll(-3)
    #     print("jump")
    # elif random == 3:
    #     pyautogui.keyDown('e')
    #     pyautogui.keyUp('e')
    #     print("impulse")




def land_mine():
    # land mine

    pyautogui.keyDown('t')
    pyautogui.keyUp('t')


def jump():
    # jump

    pyautogui.scroll(-3)

def impulse_func():
    # impulse

    pyautogui.keyDown('e')
    pyautogui.keyUp('e')




rand_time = random.randint(10,20)

start_time = time.time()


interval = rand_time * 60  # random minutes in seconds


last_press_time = time.time()

while True:

    current_time = time.time()

    elapsed_time = current_time - start_time

    if current_time - last_press_time >= interval:
        # Press the F5 key
        pyautogui.keyUp('f5')
        pyautogui.keyDown('f5')
        pyautogui.moveTo(1373, 103)
        pyautogui.mouseDown(button='left')
        pyautogui.mouseUp(button='left')
        print("Pressed F5 at", time.strftime('%H:%M:%S', time.localtime()))
        # Update the last press time
        last_press_time = current_time

    # Pause the program for 1 second
    time.sleep(1)

    choice = random.randint(1, 20)

    # jump
    if choice == 1:
        jump()
        print("jump")
    if choice == 9:
        jump()
        print("jump")

        pyautogui.mouseDown(button='left')
        time.sleep(1.55)
        pyautogui.mouseUp(button='left')

    if choice == 12:
        jump()
        print("jump")

    # impulse
    elif choice == 2:
        impulse_func()
        print("IMPULSE")
        pyautogui.sleep(0.3)
    elif choice == 13:
        impulse_func()
        print("IMPULSE")
        pyautogui.sleep(0.3)

        pyautogui.mouseDown(button='left')
        time.sleep(2)
        pyautogui.mouseUp(button='left')

    # land mine
    elif choice == 3:
        land_mine()
        print("land mine")
        pyautogui.sleep(0.3)

        pyautogui.mouseDown(button='left')
        time.sleep(2.5)
        pyautogui.mouseUp(button='left')

    elif choice == 10:
        land_mine()
        print("land mine")
        pyautogui.sleep(0.3)

    elif choice == 11:
        land_mine()
        print("land mine")
        pyautogui.sleep(0.3)

        pyautogui.mouseDown(button='left')
        time.sleep(2.2)
        pyautogui.mouseUp(button='left')

    elif choice == 15:
        land_mine()
        print("land mine")

        pyautogui.mouseDown(button='left')
        time.sleep(1.8)
        pyautogui.mouseUp(button='left')
        pyautogui.sleep(0.3)
    elif choice == 16:
        land_mine()
        print("land mine")
        pyautogui.sleep(0.3)

    elif choice == 18:
        land_mine()
        print("land mine")
        pyautogui.sleep(0.3)

    # main
    elif choice == 4:
        main_func()
        print("main func")
    elif choice == 5:
        main_func()
        print("main func")

        pyautogui.mouseDown(button='left')
        time.sleep(1.5)
        pyautogui.mouseUp(button='left')
    elif choice == 6:
        main_func()
        print("main func")
    elif choice == 7:
        main_func()
        print("main func")

        pyautogui.mouseDown(button='left')
        time.sleep(1.5)
        pyautogui.mouseUp(button='left')
    elif choice == 8:
        main_func()
        print("main func")
    elif choice == 14:
        main_func()
        print("main func")
    elif choice == 17:
        main_func()
        print("main func")

        pyautogui.mouseDown(button='left')
        time.sleep(1.5)
        pyautogui.mouseUp(button='left')

    elif choice == 19:
        main_func()
        print("main func")

        pyautogui.mouseDown(button='left')
        time.sleep(1.5)
        pyautogui.mouseUp(button='left')






    if keyboard.is_pressed("q"):
        break
        endTime = time.time() - start_time
        print(endTime)







    # If the "q" key is pressed, break out of the loop



