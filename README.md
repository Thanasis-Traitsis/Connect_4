# Connect 4 ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/icon2.png)
This is the first project that I have worked on as a student. Connect Four is a two-player connection board game, in which the players choose a color ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/RP2.png) or ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/YP2.png) and then take turns dropping colored tokens into a 7-column, 6-row vertically suspended grid. The pieces fall straight down, occupying the lowest available space within the column. The objective of the game is to be the first to form a horizontal, vertical, or diagonal line of four of one's own tokens

![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/connect_4.png)

## Entities


### Board
---------

Το board είναι ένας πίνακας, ο οποίος στο κάθε στοιχείο έχει τα παρακάτω:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `x`                      | coordinate x                                 | 1..7                                |
| `y`                      | coordinate y                                 | 1..6                                |
| `piece_color`            | The color of the pawn                        | 'R','Y', null                       |
| `piece`                  | The pawn that exists                         | 'P', null                           |
| `moves`                  | A table with the available cordinates (x,y) that the pawn can move |   |


### Players
---------

O κάθε παίκτης έχει τα παρακάτω στοιχεία:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `username`               | Όνομα παίκτη                                 | String                              |
| `piece_color`            | To χρώμα που παίζει ο παίκτης                | 'R','Y'                             |
| `token  `                | To κρυφό token του παίκτη. Επιστρέφεται μόνο τη στιγμή της εισόδου του παίκτη στο παιχνίδι | HEX |


### Game_status
---------

H κατάσταση παιχνιδιού έχει τα παρακάτω στοιχεία:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `status  `               | Κατάσταση             | 'not active', 'initialized', 'started', 'ended', 'aborded'     |
| `p_turn`                 | To χρώμα του παίκτη που παίζει        | 'R','Y',null                              |
| `result`                 | To χρώμα του παίκτη που κέρδισε |'R','Y',null                              |
| `last_change`            | Τελευταία αλλαγή/ενέργεια στην κατάσταση του παιχνιδιού         | timestamp |
