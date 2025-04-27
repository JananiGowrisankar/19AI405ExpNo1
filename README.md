<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Janani Gowrisankar </h3>
<h3>Register Number: 212224100022</h3>


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

<H3>PROGRAM</H3>

```
class VacuumCleanerAgent:
  def init(self): # Initialize the agent's state (location and dirt status)
  self.location = "A" # Initial location (can be "A" or "B")
  self.dirt_status = {"A": False, "B": False} # Initial dirt status (False means no dirt)
  def move_left(self):
    # Move the agent to the left if possible
    if self.location == "B":
        self.location = "A"

def move_right(self):
    # Move the agent to the right if possible
    if self.location == "A":
        self.location = "B"

def suck_dirt(self):
    # Suck dirt in the current location if there is dirt
    if self.dirt_status[self.location]:
        self.dirt_status[self.location] = False
        print(f"Sucked dirt in location {self.location}")

def do_nothing(self):
    # Do nothing
    pass

def perform_action(self, action):
    # Perform the specified action
    if action == "left":
        self.move_left()
    elif action == "right":
        self.move_right()
    elif action == "suck":
        self.suck_dirt()
    elif action == "nothing":
        self.do_nothing()
    else:
        print("Invalid action")

def print_status(self):
    # Print the current status of the agent
    print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")
```

<H3>Example usage:</H3>

agent = VacuumCleanerAgent()

<H3>Move the agent, suck dirt, and do nothing</H3>

agent.perform_action("left") 
agent.print_status() 
agent.perform_action("suck") 
agent.print_status() 
agent.perform_action("nothing") 
agent.print_status()

<H3>OUTPUT</H3>

<img width="746" alt="Screenshot 2025-04-27 at 16 56 49" src="https://github.com/user-attachments/assets/45a4d91b-d321-48d3-a7d9-0bb0120bc0ec" />


<H3>RESULT</H3>
Thus, an AI agent is developed.
