# Connect 4 ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/icon2.png)
This is the first project that I have worked on as a student. Connect Four is a two-player connection board game, in which the players choose a color ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/RP2.png) or ![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/YP2.png) and then take turns dropping colored tokens into a 7-column, 6-row vertically suspended grid. The pieces fall straight down, occupying the lowest available space within the column. The objective of the game is to be the first to form a horizontal, vertical, or diagonal line of four of one's own tokens

![alte text](https://github.com/Thanasis-Traitsis/Connect_4/blob/main/img/connect_4.png)

## Entities


### Board
---------

Το board είναι ένας πίνακας, ο οποίος στο κάθε στοιχείο έχει τα παρακάτω:


| Attribute                | Description                                  | Values                              |
| ------------------------ | -------------------------------------------- | ----------------------------------- |
| `x`                      | H συντεταγμένη x                             | 1..7                                |
| `y`                      | H συντεταγμένη y                             | 1..6                                |
| `piece_color`            | To χρώμα του πιονιού                         | 'R','Y', null                       |
| `piece`                  | Το πιόνι που υπάρχει                         | 'P', null                           |
| `moves`                  | Πίνακας με τα δυνατά τετράγωνα (x,y) που μπορεί να μετακινηθεί το πιόνι. Αν δεν υπάρχει πιόνι, ή δεν έχει κάνει login ο χρήστης, ή δεν έχει ξεκινήσει το παιχνίδι ή αν δεν υπάρχουν κινήσεις, τότε το πεδίο δεν υπάρχει. |   |


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
