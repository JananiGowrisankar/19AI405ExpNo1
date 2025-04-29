<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Janani Gowrisankar</h3>
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

<h3>Program:</h3>

```

import random

class Patient:
    def __init__(self, location):
        self.location = location
        self.temperature = random.uniform(97.0, 103.0)  # Random temperature between 97 and 103 degrees

    def is_unhealthy(self):
        return self.temperature > 98.5

class MedicinePrescribingAgent:
    def __init__(self):
        self.performance = 0
        self.current_location = 0  # Starting at Room 0

    def sense(self, patient):
        return patient.location, patient.temperature

    def treat(self, patient):
        if patient.is_unhealthy():
            print(f"Treating patient at Room {patient.location} with temperature {patient.temperature:.1f}°F.")
            self.performance += 10  # Increment performance for successful treatment
            patient.temperature = 98.0  # After treatment, temperature normalized
        else:
            print(f"Patient at Room {patient.location} is healthy (Temperature: {patient.temperature:.1f}°F). No treatment needed.")

    def move(self, new_location):
        if self.current_location != new_location:
            print(f"Moving from Room {self.current_location} to Room {new_location}.")
            self.performance -= 1  # Decrement performance for movement
            self.current_location = new_location

    def act(self, patients):
        for _ in range(5):  # Simulate 5 rounds of checking and treating
            patient = random.choice(patients)
            location, temperature = self.sense(patient)

            self.move(location)
            self.treat(patient)

        print(f"\nFinal Performance Score: {self.performance}")

# Simulation setup
def main():
    # Two rooms with one patient each
    patients = [Patient(location=0), Patient(location=1)]

    agent = MedicinePrescribingAgent()
    agent.act(patients)

if __name__ == "__main__":
    main()
```
<h3>Output:</h3>

![Screenshot 2025-04-29 092304](https://github.com/user-attachments/assets/0491a8ea-d971-448a-b406-de7c32b92e99)

<h3>Result:</h3>
Thus, the PEAS description for the given AI problem and develop an AI agent is successfully implemneted.

