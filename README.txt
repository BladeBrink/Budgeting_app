
Requirements:

Tkinter library 
Sqlight3
Datetime Library 
Pandas Library 
matplotlib.pyplot

Lines 1-7: Importing the required libraries

Lines 10 - 24: This piece of code is called when the "Set Budget" button is clicked in the GUI. It allows for the creation of a table called budget and drops the old budget table which contained the old budget set by the user. When creating the table, it connects to the DB called "Budgeting.db"

Lines 27 -39: This function is called when the user clicks the "Set New Goal" button in the main page of GUI. This function deletes all items in the canvas and creates new buttons, labels and Entry boxes for returning to the main menu, entering the new budget and setting the budget. These items are then packed into the canvas.

Lines 44 - 57: This function is called when the user clicks the button "Track income" button in transaction tracking page. This function tracks the date and time at which the user clicks the button using the datetime library. The users input is got from the entry box and INSERTED into the table "income". The entry box is then cleared. 

Line 61-75: This function is called when the user clicks the button "Track expense" button in transaction tracking page. This function tracks the date and time at which the user clicks the button using the datetime library. The users input is got from the entry box and INSERTED into the table "expenses". The entry box is then cleared.

Line 79-115: This function is called when the user clicks the "view budget graph" button in the main page GUI. This function starts off by running the function mainpage() which will be explained later. It then runs a try and except function. First it trys to connect to the "budgeting" DB and retrieves the income and expense data from the "income" and "expenses" table. From there, two dataframes are created. From there the data frames are merged into one. The graph is then created using date on the x-axis and income/expense on the y-axis. If there is any error in this process, the except is run which causes a second window to pop up which notifies the user.

Lines 117-118: This is called in order to close to second window from above when the "close" button is clicked. 

Lines 121 - 135: This function is called when the "track transaction" button is clicked in the main page GUI. This functions clears the canvas and packs it with the necessary Information such as buttons, labels and entry boxes. 

Line 138 - 151: This creates the scrollbar and disable scroll bar functions. It allows for the scroll bars to be added and removed from the view transactions page.

Lines 155-195: This function is called when the user clicks the "view transactions" button in the main page of the GUI. It deletes all items from the canvas and connects to the DB. It retrieve the tables "income" and "expenses". Two dataframes are created. From there the data frames are merged into one. This is used to sort the data into the latest at the top. Next it sums up all the transactions and checks it against the relevant goal set by the user. Depending on the values, there are three different outcomes, goal not reached, goal reached and no goal set. The transaction data is then added to a frame and the frame is then aded to the canvas. 

Line 212 - 223: This function is called when the mainpage needs to be loaded. First all the items in the canvas are deleted and the main 4 buttons are added to the main GIU. 

Line 226 - 245: This function is called is the program is run. It creates all the relevant tables in the DB and creates the main root and canvas on startup. 







