# talkie-buddy
	
Project Member:
John Wen (36689164)
Nandinbold Norovsambuu(48857197)
Deka Abdi
Kaiming Zhang(40417594)

Project Description:
This is an illustration of interactive conversational program with the purpose of responding to the text input given by user. Most user's purposes are about technical support or complain for computer or laptop.
The topic added to the program's repertoire is Reading/Writing about the Reviews and Ratings of the products. The user is able to write a review about the product by simply asking bot to write a review, whereas is able to look up the reviews about products from the local saved data.

Design Choices:
Terminal class, it’s the main operation class. It create a simple GUI so that the user is typing into a nicer interface and can view a recent history of the conversation. User should begin with that class to run codes. First interactive interface ask for user input by asking user “Hello, how may i help you?” Then Code save the input as string variable "text." Then, call the BotTopic class with argument “text”.

For class BotTopic, at first using tolowerCase() to convert all user inputs to lowercase letters to simplify program. Using if condition statements to justify if user want to ask question or make complaints. Based on that, code call class Questions to detailed check input. And, making some simple greeting responses. Also, using boolean variable continuing and while loop to check if the turns of a dialogue should end or keep running.

As addition to BotTopic class, the else-if conditions were implemented in order to writing / reading the product reviews and ratings.Review and rating are included inside one condition first then user is prompted to specify which one they want to do. The FileWriter,FileReader classes were used to modify the local datas review.txt, rating.txt to write and revise the product that user wants.

SpellCheck and Dictionary classes were implemented to check the spelling of the words user enters simply by checking if the word exists inside the English dictionary - the local file words.txt - if not then checks whether the word exists after 1.appending any character at the end/front 2.eliminating any character from the front/end 3.swapping any adjacent characters . Thus the program prints out the suggestions of the words that could be meant by/misspelled by the user.

Inside RandomQuestions class, the possible random questions outside the main topics which could be asked by users are saved as keys in HashMap along with their answers as values. The JaroWinklerDistance algorithm was used to calculate the similarity rate between the questions saved and the question asked by user. If the rate is higher than 75%, RandomQuestions class returns the answer by saving the result inside the static variable close_answer.

Feature List
1. A simple GUI so that the user is typing into a nicer interface and can view a recent history of the conversation. We used the feature to let user to see what question already be asked to avoid handle same question again and again.

2. We added the extra topic to our agent’s repertoire. We add a write/ read review or rating feature in our product. To make our product can handle a customer who just want share review or get know the rating about our product.

3. We added a feature that enables our agent to give at least 5 different reasonable responses when the user enters something outside the two topics. It improves our agent’s conversation by handle the greeting and random response.

4. We added a feature that enables your agent to handle spelling mistakes of the words that your agent is supposed to recognize. It improves our agent’s conversation by auto checking the spelling. To avoid us to handle more complicated scentense.



The screen shot of features are in Readme.pdf
