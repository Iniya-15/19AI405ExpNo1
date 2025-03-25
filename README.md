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
<hr>

### Program:
```
import re

# Dictionary mapping symptoms to medicines
medicine_db = {
    "fever": "Paracetamol",
    "headache": "Ibuprofen",
    "cough": "Dextromethorphan",
    "cold": "Antihistamines",
    "sore throat": "Lozenges",
    "body pain": "Acetaminophen",
    "stomach ache": "Antacids",
    "vomiting": "Ondansetron",
    "diarrhea": "ORS Solution",
    "allergy": "Cetirizine",
    "hypertension": "Amlodipine",
    "diabetes": "Metformin"
}

def prescribe_medicine(symptoms):
    """
    Function to prescribe medicine based on symptoms.
    :param symptoms: List of symptoms entered by the user.
    :return: Recommended medicine.
    """
    prescribed_medicines = set()
    
    for symptom in symptoms:
        symptom = symptom.lower().strip()
        if symptom in medicine_db:
            prescribed_medicines.add(medicine_db[symptom])

    if prescribed_medicines:
        return f"Recommended Medicines: {', '.join(prescribed_medicines)}"
    else:
        return "No exact match found. Please consult a doctor."

# Taking user input
user_input = input("Enter symptoms separated by commas: ")
symptoms_list = re.split(r',|\s+', user_input)

# Get prescribed medicine
result = prescribe_medicine(symptoms_list)
print(result)
```
### Sample Input:
```
fever, cough, body pain
```

### Sample Output:
```
Recommended Medicines: Paracetamol, Dextromethorphan, Acetaminophen
```
### Result:
Thus the python program for developing an AI agent to prescribe medicine is succesfully done.


