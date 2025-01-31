---
layout: project
type: project
image: https://www.codeproject.com/KB/recipes/692277/1.png
title: "Goats & Tiger"
date: 2022 - Present
published: true
labels:
  - Reinforcement Learning
  - Python
  - Numpy
summary: "VIP(Vertically Integrated Project) for ECEx96 about AI and board games"
---

<img width=800 align="left" src="https://www.codeproject.com/KB/recipes/692277/1.png">

---

Before you clicked on this project, did you know about this board game "Goats and Tigers?"
If you did, cool. If not, this will be a nice intro to it.
I first heard of this game when starting my VIP classes for EE back in 2022.

As a board game, it's pretty simple, yet there is some trickery that can be pulled off especially by AI.
There are different versions and maps of the game, but here are the main rules and stipulation in our project.
We use the map shown with 3 tigers and 15 goats. Your objective as the goats is to trap the tigers, so that they
can't move. The tigers are already placed down on the map and you as the player place down the goats taking turns.
Simple huh? Well here's the catch.

The tigers can eat the goat similar to checkers. If it's the tiger turn and there's a goat with an empty postion behind it,
bye bye goat. You can only lose a certain amount of goats before you can't trap the tigers. To defend against this, you 
would place goats adjacent to one another also like checkers. Once all 15 goats have been placed, you can move one goat to 
an empty adjacent postion. Onto the Machine Learning aspects.

When I started the project, we were just learning about the Reinforcement Learning(RL) alogrithms like Q-learning. The board
was already built by previous seniors, so the seniors at the time implemented different alogrithms for the tigers. I took a
break from the project for 2 semesters, and they trained a model that would beat the goats almost everytime including real players.
The model is still beatable, but it took a group of us to take it down. RL is a apart of machine learning in which agents learn to 
interact with an environment through actions to maximize rewards. You can check out more info on RL below:

<a src="https://en.wikipedia.org/wiki/Reinforcement_learning/">https://en.wikipedia.org/wiki/Reinforcement_learning </a>
