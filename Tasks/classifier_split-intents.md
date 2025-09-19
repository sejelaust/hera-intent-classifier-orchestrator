## Overall goal: Create a classifier that will based on a user input be able to classify split question intents

### Detailed job description
The classifier gets the filtered configs/split-intents.json and the API input "user_input". Here its task is to classify if any of the sub-intents are being mentioned in the user_input and then output the matched sub-intent IDs. It should return a list of the recognized sub-intents. 

The LLM classifier should should get the user input, filtered configs/split-intents.json and the llm classification instructions. 

It should first add a "reason" for its classification, then it should output a boolean "classified" true if one or more sub intents was classified and false if none where classified and lastly a list "sub-intents-classified" containing the ID or IDs of the classified sub intents. Use the examples to help classify the intents.

Use langchain and pydanticAI. 


The split-intent config is setup like the following:

{
    "<main split intent id>": {
        "<sub-intent id 1>: [
            <list of examples used to help classify the sub-intent>
        ],
        "<sub-intent id 2>" [
            <list of examples used to help classify the sub-intent>
        ]
    },
    "<main split intent id 2>": {
        "<sub-intent id 1>: [
            <list of examples used to help classify the sub-intent>
        ],
        "<sub-intent id 2>" [
            <list of examples used to help classify the sub-intent>
        ]
    }
}

