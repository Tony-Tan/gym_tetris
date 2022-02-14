# gym_tetris

an environment of game tetris

1. opencv-python is needed to display
2. the environment is like openai gym 
3. how to use:
   ```angular2html
    t = Tetris(10, 16)
    t.reset()
    is_done = False
    while not is_done:
        frame = t.draw()
        cv2.imshow('play', frame)
        action = cv2.waitKey(2000)
        if action == ord('w'):
            action = 3
        elif action == ord('a'):
            action = 0
        elif action == ord('s'):
            action = 2
        elif action  == ord('d'):
            action = 1
        else:
            action = 2
        state,reward,is_done,_ = t.step(int(action))
        print(reward)
    ```
   action 
   1. 0: go left
   2. 1: go right
   3. 2: go down
   4. 3: rotation