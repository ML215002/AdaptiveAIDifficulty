### Adaptive AI Difficulty
# Matt Law - COMP 250

## Introduction
Given the opportunity, players will optimise the fun out of a game. Whether its using only the highest rated strategies or abusing the mechanics to make the game a lot easier. To prevent the former, I will be developing an AI agent for a simple FPS that will adapt to how the player is playing in order to force them to switch up their playstyle. 

I will be using a two "brain" approach inspired by the systems used in 'Alien: Isolation' and 'Metal Gear Solid V'. This approach will use two separate scripts communicating with each other in order to calculate the best instructions. I will refer to each side as the 'Manager' and 'Control' halves.

## Base Gameplay
The AI agent I am making will be for a simple FPS game, and will require some basic movement and combat functionality as well as interactions with the game world, I.e. picking up weapons / health packs, using cover, etc. The player will also have similar capabilities as well as access to the same weapons as the AI.

Each weapon will be balanced around a rock, paper, scissors style model; with each having strengths and weaknesses against the others.

## The Manager
The 'Manager' half will keep track of all the players stats as well as their current position. It will also determine whether any incoming information requests are accessible for the 'Control' script. For example, if the player is hidden behind a wall, the control will not have access to their location. However if the player gets too far away, the manager can give vague information to push the control towards the player, stopping them from just running away.

## The Control
The 'Control' half is responsible for the agents actions and states. It will request information from the 'Manager' script and process the data recieved in order to determine what state it should be in and what instruction it should carry out next. This half will have very little information to go off, only the current statistics of the agent itself and certain base values for the different functions, I.e. health and movement speed etc.

![Image](UMLDiagram.png)

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ML215002/AdaptiveAIDifficulty/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
