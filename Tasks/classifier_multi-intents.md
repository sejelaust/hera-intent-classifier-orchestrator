## Overall goal: Create a classifier that will based on a user input be able to classify intents

### Detailed job description
The classifier gets the filtered configs/intents.json and the API input "user_input". Here its task is to classify if any of intents are being mentioned in the user_input and then output the matched intent IDs. It should return a list of the recognized intents IDs. 

The LLM classifier should should get the user input, filtered configs/split-intents.json and the llm classification instructions. 

It should first add a "reason" for its classification, then it should output a boolean "classified" true if one or more sub intents was classified and false if none where classified and lastly a list "intents-classified" containing the ID or IDs of the classified intents. 

Use langchain and pydanticAI. 


The structure of the configs/intents.json:

{
    "<intent id 1>": [
        <list of example used to classify this intent>
        ],
    "<intent id 2>": [
        <list of example used to classify this intent>
    ]
}