<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Iniya E</h3>
<h3>Register Number: 212224230096</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>
## PROGRAM:
```
import random


EMPTY = 0
DIRT = 1
GRID_SIZE = 5


grid = [[random.choice([EMPTY, DIRT]) for _ in range(GRID_SIZE)] for _ in range(GRID_SIZE)]
x, y = 0, 0 
cleaned = 0  


def move():
    global x, y
    direction = random.choice(['up', 'down', 'left', 'right'])
    if direction == 'up' and x > 0:
        x -= 1
    elif direction == 'down' and x < GRID_SIZE - 1:
        x += 1
    elif direction == 'left' and y > 0:
        y -= 1
    elif direction == 'right' and y < GRID_SIZE - 1:
        y += 1

def clean():
    global cleaned
    if grid[x][y] == DIRT:
        grid[x][y] = EMPTY
        cleaned += 1
        print(f"Cleaned dirt at position ({x}, {y})")


for step in range(10):
    print(f"Step {step + 1}: Current Position ({x}, {y}), Cleaned: {cleaned}")
    clean()
    move()

print(f"Total dirt cleaned: {cleaned}")
```
## OUTPUT:
![Screenshot 2025-03-24 090145](https://github.com/user-attachments/assets/b78b7223-fd3d-4377-9326-ac76758ec390)
## RESULT:

