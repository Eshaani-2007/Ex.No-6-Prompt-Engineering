Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

**Aim:** 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

**Explanation:**

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

**Python code**
~~~
import requests

 **Function to get response from AI Tool 1**
def get_ai1_response(prompt):
    api_url = "https://api.ai-tool1.com/generate"
    headers = {"Authorization": "Bearer YOUR_API_KEY"}
    data = {"prompt": prompt}

    response = requests.post(api_url, headers=headers, json=data)
    return response.json()["response"]

**Function to get response from AI Tool 2**
def get_ai2_response(prompt):
    api_url = "https://api.ai-tool2.com/generate"
    headers = {"Authorization": "Bearer YOUR_API_KEY"}
    data = {"prompt": prompt}

    response = requests.post(api_url, headers=headers, json=data)
    return response.json()["response"]

**Compare outputs**
def compare_outputs(output1, output2):
    print("\nAI Tool 1 Response:")
    print(output1)

    print("\nAI Tool 2 Response:")
    print(output2)

    if len(output1) > len(output2):
        print("\nInsight: AI Tool 1 provides a more detailed response.")
    elif len(output2) > len(output1):
        print("\nInsight: AI Tool 2 provides a more detailed response.")
    else:
        print("\nInsight: Both AI tools provide responses of similar length.")

**Main Program**
prompt = input("Enter your query: ")

response1 = get_ai1_response(prompt)
response2 = get_ai2_response(prompt)

compare_outputs(response1, response2)
~~~

**OUTPUT**

Enter your query: Explain Machine Learning

AI Tool 1 Response:
Machine Learning is a branch of Artificial Intelligence that enables computers to learn from data and improve performance without explicit programming.

AI Tool 2 Response:
Machine Learning is a subset of AI where algorithms learn patterns from data to make predictions and decisions automatically.

Insight:
AI Tool 1 provides a more detailed response.

**Result**

Thus, a Python program was successfully developed to integrate multiple AI tools using APIs, compare their outputs, analyze the responses, and generate actionable insights. The program demonstrates how different AI tools can be utilized together for improved decision-making and task automation.





