# wework-watson-chatbot-08.15.18

## Presentation
[Introduction to chatbot using Watson Assistant PDF](assets/wework-watson-assistant-h2o.pdf)

## IBM Cloud Sign up for this event only
[https://ibm.biz/chatbot081518](https://ibm.biz/chatbot081518)

## Additional Links
1. [Watson Assistant Service Home](https://www.ibm.com/watson/ai-assistant/)
2. [Tutorials and Documentation](https://console.bluemix.net/docs/services/conversation/getting-started.html#gettingstarted)
3. [API for different SDKs](https://www.ibm.com/watson/developercloud/assistant/api/v1/node.html?node)
4. [API Explorer ](https://watson-api-explorer.ng.bluemix.net/apis/assistant-v1)
5. [IBM Functions](https://www.ibm.com/cloud/functions)
6. [IBM Cloud Dashboard](https://console.bluemix.net/dashboard/apps/)

# Step 1: Designing Your Bot

Building a chatbot with Watson Assistant is so easy, some developers choose to dive right into the tooling. However, with a well-thought out, well-planned chatbot, the interaction with the user can lead to a much better experience that can handle edge cases. In this section, we will design the interaction between a user, Dave, and a chatbot named HungerBot.

A good question to ask yourself is, "Who is my user and what problem do they have?" Expand on the user's profile by determining what the user needs from this chatbot. Does the user have a need to book a reservation at a restaurant? Or an answer to a common question like "Where's the bathroom?" at a conference. Maybe a chatbot that handles tasks like turning on lights or other equipment. It might help to think of the chatbot as an automated version of an existing agent, such as a customer service agent. Look at existing processes that include repeated manual processes, which can sometimes be augmented with chatbots.

Training a chatbot is like training a human agent. You will train the chatbot with the knowledge of certain tasks (intents) and things that these tasks interact with (entities). These components are then combined to create a dialog tree that can take one or more paths to respond to the user's request.

In the following steps, we have provided a sample restaurant chatbot that handles reservations for a restaurant. On the right side, it's your turn to create your own chatbot. Fill in the blanks to design your chatbot.

1. Envision the user that interacts with the bot.

    |Example:|Your turn:|
    |------------------------------------------------|------------------------------------------|
    |A user, named Dave, needs to book a table at the restaurant.|A user, named _______________________, needs to _______________________________________.|

2. Now, let's give the chatbot a name and describe the overall function it can help with.

    |Example:|Your turn:|
    |------------------------------------------------|-----------------------------------------|
    |The chatbot, named HungerBot, can help the user with common tasks at a restaurant.|The chatbot, named _______________________, can help the user with ________________________.|

3. It can be helpful to take a snapshot of an existing dialogue and then break it down into intents and entities. A sample conversation is shown below. Keep the conversation simple…you can always add more complex logic later.

    |Example:|Your turn:|
    |------------------------------------------------|-----------------------------------------|
    |HungerBot: Hi, I'm HungerBot. You can ask to reserve a table and more.|Bot: |
    |Dave: I want to book a table.|User: |
    |HungerBot: What type of cuisine would you like?|Bot: |
    |Dave: I like American food|User: |
    |HungerBot: When do you want to book a table?|Bot: |
    |Dave: Tonight|User: |
    |HungerBot: How many people will be coming?|Bot: |
    |Dave: Five people|User: |
    |HungerBot: Excellent! Here are the details of your booking.|Bot: |

4. Let's start with the action the user wants to do, which is referred to as an intent. Write a human-friendly description of the action the user is wanting to perform. List at least five ways the user might phrase this action. Lastly, add a label, like a variable name in code (alpha-numeric, underscores, etc.), that can be used later as a reference.

    |Example:|Your turn:|
    |------------------------------------------------|-----------------------------------------|
    |Intent: book a reservation|Intent: |
    |Variations||
    |1.  Reserve a table|1.|
    |2.  Book a reservation|2.|
    |3.  Make a reservation|3.|
    |4.  Secure a reservation|4.|
    |5.  Schedule a reservation|5.|
    |Label: #book_reservation|Label: #|

  	If you find that you don't have many variations, invite a friend (or a real user!) to suggest how they would ask "*to book a reservation.*" In the real world, you could use customer interactions as a base of inspiration or use a thesaurus.

5. Another component to training a chatbot is recognizing objects, which is referred to as an entity. This example reservation system can differentiate different types of cuisine. We add a type of cuisine to booking a reservation.

    |Example:|Your turn:|
    |------------------------------------------------|-----------------------------------------|
    |Entity: type of cuisine|Entity:|
    |Variations:||
    |1. Mexican|1.|
    |2. Chinese|2.|
    |3. American|3.|
    |4. Italian|4.|
    |5. Mediterranean|5.|
    |Label: @cuisine|Label: @|

    We could add time and number entities, however, there are some built-in system entities provided by IBM, like numbers, dates, and times, that the HungerBot will use. If you have another entity, define the additional entity in a new table.

In the Dialog editor of Watson Assistant, we can now setup logic to step the user through the conversation. In the next section, we will use this design to train the Watson Assistant service.
    
# Step 2: Train the bot

Please refer to [this lab](https://github.com/lidderupk/chatbot-workshop/blob/master/training.md) to train Watson Assistant.
