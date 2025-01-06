# Video Game Solution Code Prompt

Please generate the entire JavaScript code for a simple platformer game where the player must jump over obstacles. The following logical expressions describe the entire game flow and behavior. Upon pasting this prompt, the solution should be automatically generated and should not ask for any additional clarifications. The code should include HTML, CSS, and JavaScript, with everything needed to recreate the game exactly as described below.

## Game Logic Expression:

1. **initializeGame()** → `score = 0 ∧ gameOver = false ∧ gameRunning = true ∧ playerPosition = {left: 50px, bottom: 50px} ∧ obstacles = [] ∧ Display(scoreDisplay, debugDisplay) ∧ AddEventListener('keydown', handlePlayerInput) ∧ AddEventListener('keydown', handleRestartInput)`
2. **player**: `{left: 50px, bottom: 50px}, isJumping = false`
3. **Player canJump()** ↔ `isJumping = false`
4. **Player jumps()** → `player.bottom += 50px ∧ isJumping = true`
5. **gravity applies when isJumping = false** → `player.bottom -= 2px`
6. **obstacle** = `{left: 100%, bottom: random value between 0 and 200px}`
7. **Obstacle moves()** → `obstacle.left -= 2px`
8. **RemoveObstacle(obstacle)** ↔ `obstacle.left <= -20px ∧ IncrementScore()`
9. **gameLoop()** → `updateObstacles() ∧ updatePlayer() ∧ checkCollision()` called continuously with `requestAnimationFrame(gameLoop)` while `gameRunning = true`
10. **handlePlayerInput()** → listens for `keyCode = 32 (spacebar)`, if `gameRunning = true` and `isJumping = false`, `Player jumps()`
11. **handleRestartInput()** → listens for `keyCode = 82 (restart key)`, if `gameOver = true`, `resetGame()`
12. **checkCollision()** → `(player.left < obstacle.left + obstacle.width) ∧ (player.bottom < obstacle.bottom + obstacle.height)` → if collision occurs, `gameOver = true` and `Display('Game Over')`
13. **score increments by 1** when obstacle moves off screen without collision
14. **resetGame()** → `score = 0 ∧ gameOver = false ∧ gameRunning = true ∧ playerPosition = {left: 50px, bottom: 50px} ∧ obstacles = []` and reinitializes game loop and UI elements
15. **debugInfo()** → `Display score, gameOver status, number of obstacles, and player position for debugging purposes`
16. **Constraints**:
    - `gameRunning = true` → `gameLoop()` runs continuously.
    - `gameOver = true` → stop `gameLoop()` and show 'Game Over'.
    - `obstacle.left <= -20px` → RemoveObstacle and IncrementScore().
    - `player.bottom >= 0px` (cannot fall below ground level)

---

## Instructions:
1. Copy and paste the above prompt into ChatGPT.
2. The code will be automatically generated, including:
   - HTML to create the game canvas and display areas.
   - CSS to style the game elements.
   - JavaScript for the game logic, including player movement, obstacles, collisions, scoring, and game restart functionality.

---

Once pasted, this prompt will generate the entire code for the game in one go. It will include the game mechanics as described, with a player jumping to avoid obstacles, a restart mechanism, score tracking, and debugging tools. The generated code should work correctly without requiring further modifications.
