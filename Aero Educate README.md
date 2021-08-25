# Aero-Educate

Aero Educate is another project developed for my Game Development module. The assignment brief was to create a 3D education game and had a number of requirements such as: having a quiz or learning element,
implementation of an AI co-learner that can assist the user, changes made to the physics engine, having different difficulty levels, etc. The project met all of the requirements and received an A+.

The game itself is an aviation history game. It combines elements of an arcade flying game along with a multiple-choice quiz to teach the player about aviation history. The player can earn points by
flying through hoops positioned on the level or by correctly answering questions in the quiz. 

### Key Features and Design choices 

The game uses a modified version of the flight controls provided in the Unity standard assets pack and also uses models found on the Unity asset store. Given that the game was being developed 
for children and teens the controls were kept relatively simple and support for a PS4 controller was also implemented.

The game loop is focused on getting the highest score possible. Players achieve this by flying through checkpoints for 100 points and answering questions for 500 points. Checkpoints and questions can only 
be activated once to prevent players accumulating infinite points. 

The quiz element of the game tests the players knowledge on aviation history. When approaching a question point, the game speed slows to allow the player time to read the question that appears
on their HUD and to pick their answer. Three checkpoints are positioned in front of the player with an answer above each. To answer a question the player needs to fly through one of the checkpoints. 
As this is an education game and not meant to be competitive, there is no penalty for an incorrect answer however, a correct answer will reward the player with 500 points. 

The quiz is fully randomised to prevent players from learning off a potential pattern in the quiz. There are two pools of questions, an easy and a hard pool, that depends on the level difficulty.
This is done by having a "Question" object which has the variables of a string for the question, a string for the answer, and a list of strings for wrong answers. On the launch of the level, a random selection
of question objects is taken from the question pool to be used in the level. 

The AI co-learner was implemented as another plane that can assist the player on the easy level. When approaching a question, the player can activate the AI named "Danny boy" and it will fly through
the correct checkpoint. This shows the player the answer to the question by they must still fly through it themselves. 

As this is a game for children and teens, a focus was placed on the game being forgiving. The checkpoints are intangible and there is no punishment for collision with the ground. Bounding boxes are placed
on all sides of the level that when crossed respawn the player just in front of the last checkpoint they crossed. Another idea that was not implemented but that was considered was a respawn button that when 
pressed would also respawn them in front of the last crossed checkpoint.



### Video and Screenshots

**[Aero Educate Demo Video](https://www.youtube.com/watch?v=VO6v-U-r_ro)**


![A2_finalbuild Screenshot 2021 08 25 - 23 16 42 55](https://user-images.githubusercontent.com/62139085/130871995-8c739dd1-bdcb-4cc6-b140-d8cf8a9e0b3f.png)
![A2_finalbuild Screenshot 2021 08 25 - 23 16 51 03](https://user-images.githubusercontent.com/62139085/130872001-2cd9d785-fd68-4293-ae93-668bd4a2a18c.png)
![A2_finalbuild Screenshot 2021 08 25 - 23 17 35 12](https://user-images.githubusercontent.com/62139085/130872005-df24e468-7452-4537-a404-85bc55918fa4.png)
![A2_finalbuild Screenshot 2021 08 25 - 23 19 09 56](https://user-images.githubusercontent.com/62139085/130872011-85f19920-ee63-4148-8537-ca4fddbc6bdd.png)
![A2_finalbuild Screenshot 2021 08 25 - 23 19 37 40](https://user-images.githubusercontent.com/62139085/130872019-997e745c-95f1-4c0c-9856-546c522519f2.png)
![A2_finalbuild Screenshot 2021 08 25 - 23 19 28 28](https://user-images.githubusercontent.com/62139085/130872023-7a3e2099-65ba-4c8d-8338-a5187b7aeb8f.png)
