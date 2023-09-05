## Java Spring Boot Client for Telegram Bot 
## Telegram Bot for Animal Shelter
## Authors: Alexander Gerb, Mikhail Schechin, Vadim Charushnikov  

This project involves creating a Telegram bot that responds to common questions from people regarding what they need to know and understand in order to adopt an animal from a shelter.

## Technologies

- Java 17
- Maven
- Spring Boot
- Spring Web
- Spring Data
- Spring JPA
- GIT
- REST
- Swagger
- Stream API

**SQL:**

- PostgreSQL

## User Functionality

### Stage 0: Query Determination
<details>
<summary>Description</summary>

This is the initial interaction point between the bot and the user.

- The bot greets the new user, introduces itself, and presents a menu to choose the purpose of the user's query:
  - Retrieve information about the shelter (Stage 1).
  - Learn how to adopt a dog from the shelter (Stage 2).
  - Request a pet report (Stage 3).
  - Request a volunteer.
- If none of the options match, the bot can summon a volunteer.
- For returning users, the new interaction starts with choosing the purpose of the user's query.
</details>

### Stage 1: Consultation with a New User
<details>
<summary>Description</summary>

At this stage, the bot provides introductory information about the shelter: its location, working hours, access rules, and guidelines for being inside the shelter and interacting with dogs.

- The bot greets the user.
- The bot can provide information about the shelter.
- The bot can provide the shelter's schedule and address, along with directions.
- The bot can provide general safety recommendations within the shelter premises.
- The bot can record contact details for communication.
- If the bot cannot answer questions, it can summon a volunteer.
</details>

### Stage 2: Consultation with a Prospective Pet Owner from the Shelter
<details>
<summary>Description</summary>

At this stage, the bot assists potential pet adopters in understanding both bureaucratic (contract requirements) and practical (preparing for life with a dog) aspects of adopting a shelter dog.

The main goal is to provide comprehensive information on preparing for the new addition to the family.

- The bot greets the user.
- The bot can provide guidelines for getting acquainted with the dog before adopting.
- The bot can list the necessary documents for adopting a dog from the shelter.
- The bot can offer transportation advice for the pet.
- The bot can provide recommendations for preparing the home for a puppy.
- The bot can provide recommendations for preparing the home for an adult dog.
- The bot can offer advice on accommodating a dog with special needs (vision, mobility).
- The bot can provide initial communication advice with a dog from a professional canine trainer.
- The bot can provide recommendations for reliable canine trainers for future reference.
- The bot can list reasons for potential adoption refusal.
- The bot can record contact details for communication.
- If the bot cannot answer questions, it can summon a volunteer.
</details>

### Stage 3: Pet Maintenance
<details>
<summary>Description</summary>

After a new pet owner adopts a dog from the shelter, they are required to provide daily reports on the pet's well-being for the first month. The daily report includes the following information:

- Pet photo.
- Pet diet.
- General well-being and adaptation to the new environment.
- Behavioral changes: shedding old habits, adopting new ones.

Reports are submitted daily, with no time constraints. Volunteers review the reports every two to three days. If the adopter fails to submit a report, the bot sends reminders. If more than two days pass, the bot contacts the volunteer to communicate with the adopter.

After the 30-day period, volunteers decide whether the dog remains with the owner or not. The trial period can be passed, extended, or failed.

- The bot can provide a daily report form.
- If the user only submits a photo, the bot can request text.
- If the user only submits text, the bot can request a photo.
- The bot can issue a warning if a report is incomplete (volunteer's role):
  "Dear adopter, we noticed that you're not filling out the report in sufficient detail. Please take this task more seriously. Otherwise, shelter volunteers will be obligated to personally inspect the dog's living conditions."
- If the adopter successfully completes the trial period, the bot congratulates them with a standard message.
- If additional trial period time is assigned, the bot notifies the adopter and specifies the number of additional days.
- If the adopter fails the trial period, the bot informs them and provides instructions for the next steps.
- If the bot cannot answer questions, it can summon a volunteer.
</details>


