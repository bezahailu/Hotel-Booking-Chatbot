# Hotel-Booking-Chatbot
<h2>What is AWS?</h2>
Amazon Web Services (AWS) is an on-demand cloud computing platform created by Amazon. It enables organizations to deploy, manage, and build applications within the cloud. 
<br />
<h2>What is Amazon Lex?</h2>
Amazon Lex is a service within AWS that adds capabilities to applications built within the platform. Such as conversational features using voice and text. With Amazon Lex, developers can create chatbots to automate tasks, find information, and provide customer support. 
<br />
<h2>Description</h2>
The project consists of a chatbot built in AWS. The chatbot allows users to create a hotel reservation within the city of their choosing. 
<br />
<br />

# STEP 1: CONFIGURING THE CHATBOT
1. After creating an AWS account, go to Amazon Lex Service (https://us-east-1.console.aws.amazon.com/lex/home?region=us-east-1) 
2. Click on “Get Started”
3. Click on “Create Bot”
<img width="1220" alt="Screenshot 2024-02-23 at 14 02 33" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/748d7ab9-57e3-4083-ad2c-ce33491a05c0">
4. Under “Creation Method”, click “Create a blank bot”
<img width="815" alt="Screenshot 2024-02-23 at 14 05 50" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/1962f522-eedb-4871-9e19-2dd67fc6ea08">

5. Under “Bot Configuration”, you can choose a custom name
- The name for the bot will be HotelBooking
6. Under “IAM permissions”, click on “Create a role with basic Amazon Lex permissions”
7. Under “Children’s Online Privacy Protection Act” click “No”
8. Under “Idle session timeout”, select 5 minutes
9. Under “Add Language to Bot”, select the following settings and click on “Save”
<img width="1027" alt="Screenshot 2024-02-23 at 14 12 31" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/9dfddf20-bebb-414b-8c64-6f55338c240e">
<br />
<br />

# STEP 2: CREATING SLOTS AND INTENTS
1. After configuring the bot, you will automatically be redirected to create an intent
2. Under “Intent Details”, type BookHotel
<img width="784" alt="Screenshot 2024-02-26 at 12 23 51" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/13c7ed2f-238e-4c88-9372-988a96d2e131">

3. Under “Sample “Utterances”, write the following phrases and click on “Add Utterance”
- Book a hotel
- I want to make a hotel reservation
- Book a 3 night stay in London

NOTE: DO NOT ADD ANY PUNCTUATION AT THE END OF EACH UTTERANCE
<img width="801" alt="Screenshot 2024-02-26 at 12 26 20" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/af169dcb-a07f-4fe9-875f-85eef68bb9e1">

4. Double click the word “London” on the utterance “Book a 3 night stay in London”
<img width="767" alt="Screenshot 2024-02-26 at 12 28 21" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/d446edb9-c541-4dad-8333-804070c3987e">

- Select AMAZON.City

5. Double click the number “3” on the utterance “Book a 3 night stay in London”
6. Select AMAZON.Number
<img width="857" alt="Screenshot 2024-02-26 at 12 30 29" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/0ed692c6-c57c-44df-9c88-3323783c5239">

7. Scroll down to “Slots”
8. Under the numerical slot, change the name from 3 to “Nights”
- Add the prompt “How many nights will you be staying?”
<img width="792" alt="Screenshot 2024-02-26 at 12 32 05" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/d44c3ff4-2077-4ee5-a7db-07a3b85aa442">

9. Under the London slot, change the name from London to “Location”
- Add the prompt “What city will you be staying in?”
- Click the box that says “Required for this intent”
<img width="770" alt="Screenshot 2024-02-26 at 12 39 04" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/d5ff78b7-f63e-4567-a984-7d53860418ff">

10. Add some more slots
- Click “Add slot”
<img width="770" alt="Screenshot 2024-02-26 at 12 39 04" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/432c4be4-17d3-4019-bc26-03d483f26c87">

11. Click “Save intent” at the bottom right of the page
12. Go to “Slot types” on the left side of the page 
13. Click on “Add slot type”
14. Name the slot “RoomType
<img width="607" alt="Screenshot 2024-02-27 at 12 39 17" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/39d43dd2-7bba-4a10-a83f-e82d2a418b4c">

15. Under slot type values, add the following values and save the slot type
<img width="678" alt="Screenshot 2024-02-27 at 12 42 15" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/bb8f51e3-d73e-4710-ac86-8af45122e637">

16. Go back to the intents page and click on HotelBooking
17. Under slots, add the RoomType slot and type in the following:
<img width="603" alt="Screenshot 2024-02-27 at 12 45 29" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/897a571e-e4b4-44c7-b039-88cadc3c3068">

18. To add a confirmation prompt, go to the “confirmation” section
19. Make sure the “active” toggle is on
20. Type in the following. Make sure the variables are included. 
<img width="680" alt="Screenshot 2024-02-27 at 13 04 39" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/202d65fb-2000-4383-a0e8-c0341b1d9676">

21. Go to the “Fulfillment” section
- Type in the following to enter a fulfillment message
<img width="664" alt="Screenshot 2024-02-27 at 13 18 48" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/ecc4ed4f-b0dd-4248-8e05-654038885f3c">

22. Save the intent
23. Click on “Build” on the top right of the page
24. Once the building process is complete, click on “Test”
25. Type in some prompts to check if the chatbot is fully functioning
<img width="332" alt="Screenshot 2024-02-27 at 12 59 56" src="https://github.com/bezahailu/Hotel-Booking-Chatbot/assets/48112769/cae33335-fd41-4af2-a238-3303b1448d94">

NOTE: YOU CAN CHANGE THE ORDER OF THE SLOTS TO ASK THE QUESTIONS IN A CERTAIN ORDER













