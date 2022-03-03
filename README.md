# Connect 4 ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/icon2.png)
This is the first project that I have worked on as a student. Connect Four is a two-player connection board game, in which the players choose a color ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/RP2.png) or ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/YP2.png) and then take turns dropping colored tokens into a 7-column, 6-row vertically suspended grid. The pieces fall straight down, occupying the lowest available space within the column. The objective of the game is to be the first to form a horizontal, vertical, or diagonal line of four of one's own tokens

![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/connect_4.png)

## Entities


### Board
---------

The board is a table, in which each element has the following:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `x`                      | Coordinate x                                 | 1..7                                |
| `y`                      | Coordinate y                                 | 1..6                                |
| `piece_color`            | The color of the pawn                        | 'R','Y', null                       |
| `piece`                  | The pawn that exists                         | 'P', null                           |
| `moves`                  | A table with the available coordinates (x,y) that the pawn can move |   |


### Players
---------

Every player has the following attributes:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `username`               | The name of the player                               | String                              |
| `piece_color`            | The color of the pawn               | 'R','Y'                             |
| `token  `                | A random generated number for a player, everytime the game starts | HEX |


### Game_status
---------

The status of the game should have the following attributes:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `status  `               | current status of the game            | 'not active', 'initialized', 'started', 'ended', 'aborded'     |
| `p_turn`                 | The color of the player that makes the next move      | 'R','Y',null                              |
| `result`                 | The color of the player that won |'R','Y',null                              |
| `last_change`            | Last change / action in game mode        | timestamp |
