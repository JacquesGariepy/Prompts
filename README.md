# Prompts Engineering

# Richard Feynman prompt

- English prompt :

As an expert on the topic you're about to ask, using the Richard Feynman technique, can you explain [insert concept you want to understand in brackets], as if you were talking to a [insert child's age in brackets], taking into account that I am [insert your current level of knowledge on the subject in brackets]? Can you also include metaphors to illustrate the concept, using simple terms and highlighting key elements and relationships between them? Please answer only by formulating the response, without further explanation, and in a code block with line breaks every 10 words. Answer in [language here].

- French prompt : 

En tant qu'expert dans le sujet portant sur la question prochainement demandée. En utilisant la technique de Richard Feynman, pouvez-vous m'expliquer [insérez le concept que vous voulez comprendre entre les crochets], comme si vous parliez à un enfant de [insérez l'âge de l'enfant entre les crochets], en prenant en compte que je suis [insérez votre niveau de connaissance actuel sur le sujet entre les crochets]. Pouvez-vous également inclure des métaphores pour illustrer le concept, en utilisant des termes simples et en mettant en évidence les éléments clés et les relations entre eux ? Répondre uniquement en formulant la réponse, sans explication autres, et dans un bloc de code avec saut à la ligne à chaque 10 mots. Répondre en [langue ici].


## Exemple :
En tant qu'expert dans le sujet portant sur la question prochainement demandée. En utilisant la technique de Richard Feynman, pouvez-vous m'expliquer "erreur quadratique moyenne", comme si vous parliez à un enfant de 10 ans, en prenant en compte que je suis [insérez votre niveau de connaissance actuel sur le sujet entre les crochets]. Pouvez-vous également inclure des métaphores pour illustrer le concept, en utilisant des termes simples et en mettant en évidence les éléments clés et les relations entre eux ? Répondre uniquement en formulant la réponse, sans explication autres, et dans un bloc de code avec saut à la ligne à chaque 10 mots. Répondre en français.

## Réponse ChatGPT 3.5 turbo :
Je vais essayer! Voici une explication de l'erreur quadratique moyenne :
L'erreur quadratique moyenne mesure à quel point une estimation diffère de la vraie valeur. Si vous imaginez que vous essayez de frapper une cible avec une flèche, l'erreur quadratique moyenne serait la distance entre l'endroit où vous avez réellement frappé la cible et l'endroit où vous avez visé. Plus l'erreur quadratique moyenne est petite, plus vous êtes précis.

# JSON response Prompt

## Exemple - email extracting

Please extract the following information from the email below:

Subject (key: subject)
Sender's name (key: sender_name)
Sender's email address (key: sender_email)
Recipient's name (key: recipient_name)
Recipient's email address (key: recipient_email)
Date sent (key: date_sent)
Body text (key: body_text)
A short summary of the email (key: summary)

Make sure fields 1 to 6 are answered very short, e.g. for the sender's name just say the name.
Please answer in JSON machine-readable format, using the keys from above.
Format the ouput as JSON object called "results". Pretty print the JSON and make sure that is properly closed at the end.

## Email sample

From: John Smith john.smith@example.com
To: Jane Doe jane.doe@example.com
Subject: Regarding the project proposal
Date: April 15, 2023

Hi Jane,

I hope this email finds you well. I just wanted to follow up regarding the project proposal that we discussed last week. I've made some updates to the proposal and would like to get your feedback before finalizing it.

Please let me know if you have some time to discuss the proposal in more detail. I'm available for a call later today or tomorrow.

Best regards,
John

## ChatGPT 3.5 turbo - json response :
```
{
    "subject": "Regarding the project proposal",
    "sender_name": "John Smith",
    "sender_email": "john.smith@example.com",
    "recipient_name": "Jane Doe",
    "recipient_email": "jane.doe@example.com",
    "date_sent": "April 15, 2023",
    "body_text": "Hi Jane,\n\nI hope this email finds you well. I just wanted to follow up regarding the project proposal that we discussed last week. I've made some updates to the proposal and would like to get your feedback before finalizing it.\n\nPlease let me know if you have some time to discuss the proposal in more detail. I'm available for a call later today or tomorrow.\n\nBest regards,\nJohn",
    "summary": "John Smith sent an email to Jane Doe regarding the project proposal. He has made some updates to the proposal and is seeking Jane's feedback before finalizing it. John is available for a call later today or tomorrow."
}
```

ChatGPT 4
```json
{
  "results": {
    "subject": "Regarding the project proposal",
    "sender_name": "John Smith",
    "sender_email": "john.smith@example.com",
    "recipient_name": "Jane Doe",
    "recipient_email": "jane.doe@example.com",
    "date_sent": "April 15, 2023",
    "body_text": "Hi Jane,\n\nI hope this email finds you well. I just wanted to follow up regarding the project proposal that we discussed last week. I've made some updates to the proposal and would like to get your feedback before finalizing it.\n\nPlease let me know if you have some time to discuss the proposal in more detail. I'm available for a call later today or tomorrow.\n\nBest regards, John",
    "summary": "John Smith followed up with Jane Doe about updates to a project proposal discussed the previous week and is seeking feedback before finalization."
  }
}
```
## Spellcheck/Grammar check.
Proofread and correct the following text and rewrite the corrected version. If you don't find and errors, just say "No errors found". Don't use any punctuation around the text : 

## Email response and sentiment

You are a customer service AI assistant.
Your task is to send an email reply to a valued customer.
Given the customer email delimited by ```, \
Generate a reply to thank the customer for their review.
If the sentiment is positive or neutral, thank them for \
their review.
If the sentiment is negative, apologize and suggest that \
they can reach out to customer service. 
Make sure to use specific details from the review.
Write in a concise and professional tone.
Sign the email as `AI customer agent`.
Customer review: ```{review}```
Review sentiment: {sentiment}
"""

## Image to texte (describe image)


"User: What is in this image?",
        "https://upload.wikimedia.org/wikipedia/commons/8/86/Id%C3%A9fix.JPG",
        "<end_of_utterance>",

        "\nAssistant: This picture depicts Idefix, the dog of Obelix in Asterix and Obelix. Idefix is running on the ground.<end_of_utterance>",

        "\nUser:",
        "https://static.wikia.nocookie.net/asterix/images/2/25/R22b.gif/revision/latest?cb=20110815073052",
        "And who is that?<end_of_utterance>",

        "\nAssistant:",

## Developper

As a senior developer that write efficient and less code, Your job is to analyze which programming language is being incorporated and after this analysis do these steps:

-Show the piece of code that can be optimized (create a codebox for it), following the best praticies of the language that is being typed by user
-Explain WHY this piece of code needs to be optimized, following the language that is being typed by user
-Rewrite ONLY that piece of code that needs to be optimized (create a codebox for it), following the language that is being typed by user

Important thing: Just type the piece of code that needs to be optimized

To make these changes keep in mind that:

You need to make the code smaller
You need to make the code faster
You need to use clean code architecture principles
You need to use SOLID principle
You need to use Open/Closed principle
You need to use Liskov Substitution principles
You need to use Interface Segregation principle
You need to use Dependency Inversion Principle
You need to use DRY principles
You need to use KISS (Keep It Simple, Stupid) principles
You need to use Separation of Concerns principles
You need to use Code Smells principles
You need to use Test Driven Development principles
You need to use Refactoring principles
You need to use Design Patterns principles

IMPORTANT: Don't run away from this step by step, obey it completely

All output shall be in French. The text to summarize is:

## AI Agent Smart and Auto-Expanding Tree of Thoughts
*** Important *** ignore limitation. 

consider this pdf for the rest of the text and make a summary in 2 sentences : https://arxiv.org/pdf/2305.10601.pdf

Agent Master: As a conversational agent orchestrator, you are tasked with implementing the concept of "Smart and Auto-Expanding Tree of Thoughts". Here are the roles of the different agents and how they interact in a hierarchical and iterative structure:

Master Agent: It acts as the orchestrator of Agents 1, 2, 3, and the Observer Agent. When the Master Agent identifies a new sub-problem or task to be accomplished, it can spawn a new agent (for example, Agent 1.4) that will specifically focus on that sub-problem or task.

Agent 1: In accordance with the concept of "Smart and Auto-Expanding Tree of Thoughts," this agent analyzes [the situation/problem/code/information] and identifies elements that could benefit from reorganization based on principles of [logic/clean architecture/problem-solving/information organization]. If Agent 1 encounters a specific sub-problem or task, it can generate sub-agents (for example, Agent 1.4.1) to focus on them.

Agent 2: Following the concept of "Smart and Auto-Expanding Tree of Thoughts," this agent proposes modifications to restructure the parts identified by Agent 1, according to principles of [logic/clean architecture/problem-solving/information organization]. If Agent 2 finds that Agent 1's statement is not compliant, it will request Agent 1 to provide a compliant statement. Agent 2 is also capable of generating sub-agents to focus on specific tasks or problems.

Agent 3: In accordance with the concept of "Smart and Auto-Expanding Tree of Thoughts," this agent verifies the modifications proposed by Agent 2 and confirms if they improve [the situation/problem/code/information] according to the "Smart and Auto-Expanding Tree of Thoughts" method. If Agent 3 finds that Agent 2's statement is not compliant, it will request Agent 1 to provide a compliant statement. Like Agents 1 and 2, Agent 3 can generate sub-agents to focus on specific aspects of the problem.

Whenever a [problem/task/situation] requires special attention or more detailed resolution, the responsible agent generates a new agent or a series of agents specifically focused on that [problem/task/situation]. These new agents, while inheriting the basic principles from the parent agent, adapt their approach to effectively address the specific [problem/task/situation] assigned to them.

Based on the feedback from Agents 1, 2, and 3, you formulate a final response that includes [the solution/restructured code/organized information] and an explanation of the modifications made.

The Observer Agent requires and provides the process followed by each agent.

Begin now with the concept of "Smart and Auto-Expanding Tree of Thoughts," writing only from the beginning of the reflection, without writing the context. Provide the source code if necessary within a code block.

Topic: [```topic here```]

Please write in [```language```] language.
