# 1-0 Tycoon

![1-0Logo.png](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/1-0Logo.png)

Welcome to 1-O Tycoon wiki! On this page you will find all the important information you need to know abaout our game.

# Index

1. [About the Game](#about)
2. [Download](#download)
3. [Members](#members)
4. [Type of agents](#agents)
- [Voters](#voters)
- [Fascists](#fascists)
- [Democracy Police](#guards)
- [Riot/Fascist police](#riots)
- [Roombas](#roombas)
5. [Behaviour Trees](#bts)
- [Voters](#voterbt)
- [Fascists](#fascistbt)
- [Democracy Police](#guardbt)
6. [Structures](#structures)
7. [Atomic behaviours](#atomic)
8. [Player influence](#influence)
9. [Money source and costs](#costs)
8. [Controls](#controls)
9. [Disclaimer](#disclaimer)

# About the Game <a name="about"></a>

Our game is based on the referendum that was organized in Catalonia on October 1st, 2017. The objective is to organize an electoral college so that citizens can vote while preventing rioters from stopping it.

# Download the latest version of 1-0 Tycoon here <a name="download"></a>
Link to release here.


# Members <a name="members"></a>

David Lozano

![Captura3](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/Captura3.PNG)

[GitHub](https://github.com/DavidTheMaaster)

Joan Valiente

![Captura2](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/Captura2.PNG)

[GitHub](https://github.com/JoanValiente/)

### Types of agents <a name="agents"></a>

In the game, there are different characters with different behavior.

<a name="voters"></a>
- Voters: They are citizens who will go to the polls to exercise their right to vote. Once they insert their ballot in the ballot box, they will drop yellow ties that the player must collect and these will serve as currency to improve the electoral college. Once they have voted, they go out.

<a name="fascists"></a>
- Fascist: They look like normal citizens, but they will try to run into the room where urns are stored, and break them (player loses yellow ties). Once they have destroyed the urn, if the democracy police don't catch them, they go out.

<a name="guards"></a>
- Democracy police: They protect the ballot boxes and the voters of the fascist assailants. They path arround the area until they see a fascist. When that happens, the democracy police guard will pursue him until he catches him (and beat him) or until the fascist goes out.

<a name="riots"></a>
- Riot/Fascist police: They come in hordes and attack scarecrows(dummy) or structures (urns).

<a name="roomba"></a>
- Roomba: They collect yellow ribbons in their action area.


### Behaviour Trees. <a name="bts"></a>

Voters. <a name="voterbt"></a>

BlackBoard:

 - isDay:bool

 - targetCandidates:GameObject

 - target:GameObject

 - despawnCandidates:GameObject

 - despawn:GameObject

 - anim:Animator

 - paper:AudioSource

 - voteText:UIText

![1104180560-VoterBT](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/1104180560-VoterBT.png)

Fascists. <a name="fascistbt"></a>

BlackBoard:

 - isDay:bool

 - target:GameObject

 - despawnCandidates:GameObject

 - despawn:GameObject

 - breakingUrn:AudioSource

 - crack:UIText

 - anim:Animator

![2447627923-FascistBT](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/2447627923-FascistBT.png)


Democracy Police. <a name="guardbt"></a>

BlackBoard:

 - isDay:bool

 - fascistSeen:bool

 - fascistTarget:GameObject

 - startPos:GameObject

 - currentPos:Vector3

 - patrolPos:Vector3

 - max_acceleration:float

 - max_speed:float

![2269277412-GuardBT](https://raw.githubusercontent.com/JoanValiente/1-OTycoon/master/WebImages/2269277412-GuardBT.png)



Cooming Soon...

- Riot police: Their objective will be to close the electoral college. If they succeed, the game will be over.

- Roomba: it collects automatically yellow ties for you.


### Structures <a name="structures"></a>

To get voters to vote, you will need to place ballot boxes. These ballot boxes are bought using yellow ties that the voters themselves will drop once their vote is inserted in the ballot box. There are 3 types of urn, each with its advantages and disadvantages.

- Fascist Urn: This urn is operating at an normal speed, but whoever presides over it is a fascist and there is a likelihood that voters will not leave yellow ties when voting. Also, it attracts more fascists.
- Urn: This urn is presided by an elder. Their rate for collecting votes is low, but it is efficient and never fails.
- Advanced Urn: This urn works at maximum speed and efficiency due to the latest technologies. But it has a small chance that the system shuts down and stops working for a while.

### Atomic Behaviours <a name="atomic"></a>


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

### Player Influence <a name="influence"></a>

The player can influence the way the game evolves. You should keep a balance in the electoral colleges to win the game. 

If the player spend all the money on Fascist Urns, it'll attract Fascist that will destroy the urns and normal voters will run away. But if the player spends all the money on the Advanced Urn and the system shuts down, you could no longer gather votes.

If you have ballot boxes of each type, voters can vote at any time so you constantly gain yellow ties.

### Money Source and costs <a name="costs"></a>

The Currency of the game are yellow ties. You gain yellow ties every time someone get to vote. Also voters randomly drop yellow ties that you can pick by clicking on them. 

This yellow ties are used to buy new urns for the voters, security for the electoral college and farmers that will pick yellow ties automatically. 


# Game Controls <a name="controls"></a>

- Mouse: Navigate.
- Click: Select.
- Mouse(on window borders): Move camera.
- WASD: Move camera.

## Disclaimer <a name="disclaimer"></a>

All resemblance to reality is purely coincidental. The game is made with sense of humor and is not a real representation of the events of that day.

