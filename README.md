# 1-0 Tycoon

![1-0Logo.png](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/1-0Logo.png)

Welcome to 1-O Tycoon wiki! On this page you will find all the important information you need to know abaout our game.

## About the Game

Our game is based on the referendum that was organized in Catalonia on October 1st, 2017. The objective is to organize an electoral college so that citizens can vote while preventing rioters from stopping it.

# Download the latest version of 1-0 Tycoon here
Link to release here.


# Members

David Lozano

![Captura3](1-OTycoon/WebImages/Captura3.png)

[GitHub](https://github.com/DavidTheMaaster)

Joan Valiente

![Captura2](1-OTycoon/WebImages/Captura2.png)

[GitHub](https://github.com/JoanValiente/)

### Types of agents

In the game, there are different characters with different behavior.

- Voters: They are citizens who will go to the polls to exercise their right to vote. Once they insert their ballot in the ballot box, they will drop yellow ties that the player must collect and these will serve as currency to improve the electoral college. Once they have voted, they go out.
- Fascist: They look like normal citizens, but they will try to run into the room where urns are stored, and break them (player loses yellow ties). Once they have destroyed the urn, if the democracy police don't catch them, they go out.
- Democracy police: They protect the ballot boxes and the voters of the fascist assailants. They path arround the area until they see a fascist. When that happens, the democracy police guard will pursue him until he catches him (and beat him) or until the fascist goes out.


### Behaviour Trees.

Voters.

BlackBoard:

 - isDay:bool

 - targetCandidates:GameObject

 - target:GameObject

 - despawnCandidates:GameObject

 - despawn:GameObject

 - anim:Animator

 - paper:AudioSource

 - voteText:UIText

![1104180560-VoterBT](1-OTycoon/WebImages/1104180560-VoterBT)

Fascists.

BlackBoard:

 - isDay:bool

 - target:GameObject

 - despawnCandidates:GameObject

 - despawn:GameObject

 - breakingUrn:AudioSource

 - crack:UIText

 - anim:Animator

![2447627923-FascistBT](1-OTycoon/WebImages/2447627923-FascistBT)


Democracy Police.

BlackBoard:

 - isDay:bool

 - fascistSeen:bool

 - fascistTarget:GameObject

 - startPos:GameObject

 - currentPos:Vector3

 - patrolPos:Vector3

 - max_acceleration:float

 - max_speed:float

![2269277412-GuardBT](1-OTycoon/WebImages/2269277412-GuardBT)



Cooming Soon...

- Riot police: Their objective will be to close the electoral college. If they succeed, the game will be over.

- Roomba: it collects automatically yellow ties for you.


### Structures

To get voters to vote, you will need to place ballot boxes. These ballot boxes are bought using yellow ties that the voters themselves will drop once their vote is inserted in the ballot box. There are 3 types of urn, each with its advantages and disadvantages.

- Fascist Urn: This urn is operating at an normal speed, but whoever presides over it is a fascist and there is a likelihood that voters will not leave yellow ties when voting. Also, it attracts more fascists.
- Urn: This urn is presided by an elder. Their rate for collecting votes is low, but it is efficient and never fails.
- Advanced Urn: This urn works at maximum speed and efficiency due to the latest technologies. But it has a small chance that the system shuts down and stops working for a while.

### Atomic Behaviours


## Voters 

- Drop yellow tie (randomly).

- Move to urn and vote. Give player democracy points.

- Go to exit.

## Fascist

- Run and break urns. That makes player loose yellow ties and democracy points.

- Run away.

## Riot Police

- Destroy structures or scarecrowns(dummy). They comes in hordes.

- Go away.

## Democracy Police

- Path arround until they see a fascist.

- Pursue fascist.

- Hit Fascists.

## Roombas

- Collects yellow ties (on an area).

### Player Influence

The player can influence the way the game evolves. You should keep a balance in the electoral colleges to win the game. 

If the player spend all the money on Fascist Urns, it'll attract Fascist that will destroy the urns and normal voters will run away. But if the player spends all the money on the Advanced Urn and the system shuts down, you could no longer gather votes.

If you have ballot boxes of each type, voters can vote at any time so you constantly gain yellow ties.

### Money Source and costs

The Currency of the game are yellow ties. You gain yellow ties every time someone get to vote. Also voters randomly drop yellow ties that you can pick by clicking on them. 

This yellow ties are used to buy new urns for the voters, security for the electoral college and farmers that will pick yellow ties automatically. 


# Game Controls

- Mouse: Navigate.
- Click: Select.
- Mouse(on window borders): Move camera.
- WASD: Move camera.

## Disclaimer

All resemblance to reality is purely coincidental. The game is made with sense of humor and is not a real representation of the events of that day.

