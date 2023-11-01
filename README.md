# Group 4 MIST 4160 Project 1
29704 Group 4

# Team Members:
1. Ryan Kelly: [@Rjk4133](https://github.com/Rjk4133)
2. Ryan Dean: [@RDean45](https://github.com/RDean45)
3. Cameron Smith:[@camjshmitt](https://github.com/camjshmitt)
4. Mattie Garett: [@MatGar22](https://github.com/MatGar22)
5. Lilly Wood: [@lillywood21](https://github.com/lillywood1)
7. Wyatt Smith: [@wsmith1287](https://github.com/wsmith1287)

# Problem Description:
The problem that we are trying to solve has to do with the creation of a working database that consolidates data for a soccer club into a functioning model. The main entity that comprises this data and the model is the Team entity which is made up of the different teams that comprise the soccer club and includes information such as their team name and where their home field is. In addition to this, we have other entities such as data on the players that comprise these teams, the statistics for each of these players, the coaching staff that make up the soccer club, and much more. In addition to a working model, we hope to build many working queries that provide data to possible stakeholders of the soccer club to make well informed complex decisions regarding the clubs activities. With this complex data model and the many different queries we hope to deliver working data that can be used by the soccer club to operate at an increased efficiency level and deliver better value to its stakeholders.
# Data Model:
Our model is structured like a football (soccer) academy. The Teams entity represents the information stored about each of the different teams in the club including the team ID, the team name, the team’s home field and more. Teams have many matches, which is shown by the one to many identifying relationship between Teams and Teams Have Matches. Teams also have head coaches which is represented by the one to one non identifying relationship between Teams and the entity Coaching Staff. Teams have many coaches which is shown by the one to many non identifying relationship between Teams and Coaching Staff. Teams may also have many sponsors which is represented by the one to many identifying relationship between Teams and the Teams Have Sponsors entity. Teams have many players which is shown by the one to many non identifying relationship between Teams and Player Information. Teams also have captains which are represented by the one to one non identifying relationship between Teams and Player Information.

Player Information stores data like the player’s player ID, the player’s first and last name, their age and much more. Players have many statistical instances recorded which is represented by the one to many relationship between Player Information and Player Stats. Player Stats stores information pertaining to the saves, goals scored, minutes played, and penalties of each player during each match for a specific team. Players can also have many Injury Reports which is represented by the one to many identifying relationship between Player Information and Injury Report. Injury report has information regarding the injury such as the reportID, type of injury that occurred, and estimated recovery timeline.

Teams Have Matches stores information on the match date, venue and more. Teams Have Matches stores many player stats which is shown by the one to many identifying relationship between Player Stats and Teams Have Matches.

Matches stores data on the match ID, match type and more. Matches is made up of many different individual matches which is represented by the one to many identifying relationship between Match and Teams Have Matches.

Divisions store information on the division ID, the division name, the division age group, the division skill level and more. Divisions have many matches which is shown by the one to many non identifying relationship between Divisions and Match. Divisions are made up of many different teams which is represented by the one to many non identifying relationship between Divisions and Teams.

The league entity stores data on the league ID, the league name, the league president, the date founded, and much more. A league is many up of many Divisions which is represented by the one to many non identifying relationship between League and Divisions.

The Sponsor entity stores information including the sponsor ID, the sponsor name, and the phone number associated with the sponsor. A sponsor makes up a list of many different sponsors which is represented by the one to many identifying relationship between Sponsor and Teams Have Sponsors. The Teams Have Sponsors table is an associative entity created by the many to many relationship between Teams and Sponsors. The Teams Have Sponsors entity stores data such as the date of sponsorship and amount of sponsorship.

Coaching Staff stores data including the coach ID, the coach’s first and last name, the number of years they have coached, their date of birth, their date of birth, and much more. Coaching Staff at the football club report to Head Coaches which is shown by the one to many non identifying recursive relationship between Coaching Staff. Coaching Staff hold many training sessions which is represented by the one to many non identifying relationship between Coaching Staff and Training Sessions.

Training Sessions store information on the session ID, the practice date, and more. Training Sessions can require many field reservations depending on the type of drills run which is represented by the one to many identifying relationship between Training Sessions and Field Reservation. Field reservations stores data including a composite primary key of fieldID and sessionID along with data such as reservation status and the date and time reserved.
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/b740ed9c-8cea-4e99-a373-def0122ca7cb)

# Data Dictionary:
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/fd1bf9de-c141-48d6-b08c-f6f2a2337831)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/bf115d89-1977-4b77-9287-f58dc24f05bb)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/ef65353f-04c4-45bc-93dc-55118ea95b4b)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/87a95b5e-ddb7-499b-bc97-1f38174fd36f)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/cd03e9e8-0e51-4cbe-a96b-2671c5712bbe)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/d87e990d-506b-438c-b5ba-3e92917b8a92)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/402984b2-36db-41bb-a852-a1af8c9f8448)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/a53985ab-d490-46c1-a836-120a5a5cc911)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/cf43e3d2-7927-4b10-a5a0-2566259bcdb9)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/96921523-a49a-4325-b705-052310954f30)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/0adcb6e0-c79c-4394-a07c-5041e142d77c)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/324e9fe8-e00b-4818-a0aa-556cc3bd4db4)
![image](https://github.com/RDean45/MISTGroup4Project1/assets/148080144/1b5b877a-3d2d-4002-a4f1-6bddae739793)


# Ten Queries:

# Database Information:
