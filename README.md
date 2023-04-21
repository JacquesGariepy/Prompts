# Prompts Engeneering

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


Car accident reported.


Jacques Gariépy
You must extract the following information from the phone conversation below:

1. Call reason (key: reason)
2. Cause of the incident (key: cause)
3. Names of all drivers as an array (key: driver_names)
4. Insurance number (key: insurance_number)
5. Accident location (key: location)
6. Car damages as an array (key: damages)
7. A short, yet detailed summary (key: summary)

Make sure fields 1 to 6 are answered very short, e.g. for location just say the location name.

Please answer in JSON machine-readable format, using the keys from above.
Format the ouput as JSON object called "results". Pretty print the JSON and make sure that is properly closed at the end.

Phone conversation:
Hi I just had a car accident and wanted to report it. OK, I hope you're 

2 / 2


{"results": {
"reason": "car accident",
"cause": "other driver ran a red light",
"driver_names": ["John Smith", "Jane Doe"],
"insurance_number": "123456789",
"location": "Main Street",
"damages": ["rear bumper", "driver-side door"],
"summary": "John Smith and Jane Doe were involved in a car accident on Main Street. The cause of the accident was the other driver running a red light. The damages include the rear bumper and driver-side door. The insurance number provided is 123456789."
}}





Jacques Gariépy
Show me an other subject. replace the next text  : You must extract the following information from the phone conversation below:

Call reason (key: reason)
Cause of the incident (key: cause)
Names of all drivers as an array (key: driver_names)
Insurance number (key: insurance_number)
Accident location (key: location)
Car damages as an array (key: damages)
A short, yet detailed summary (key: summary)
Make sure fields 1 to 6 are answered very short, e.g. for location just say the location name.

Sure, here's an example prompt:

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





Jacques Gariépy
Continue

Here's an example email that we can use for this prompt:

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
