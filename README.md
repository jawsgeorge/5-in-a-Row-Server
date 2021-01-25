#5-in-a-Row-server

#Description
5-in-a-Row-server is a spring boot application which maintains the state of the 5-in-a-row 5 game and also exposes some REST
APIs for the clients to connect and play the game.

#Steps  to run
1. Run command : mvn clean install
2. It will generates a jar file inside the target folder 
2. Go to target jar directory
3. Run command: java -jar 5-in-a-Row-server-0.0.1-SNAPSHOT.jar
3. This starts the server application and it can accept requests from the client over http on port 8080

#REST APIS exposed:
    http://localhost:8080/api/v1/grid : This returns the state of the Connect5 Board.
	http://localhost:8080/api/v1/drop: This POST request given the playername and column number, makes the game possible. It
	also returns whether the game ended due to a draw,Win or if the grid is full.
	http://localhost:8080/api/v1/lastplayer
	This GET request returns the name of the last player who made a move.
	http://localhost:8080/api/v1/poll
	This GET request makes the asynchronous event mechanism possible for events such as waiting for turns,informing the
	other player of exits,wins,draws,etc.
	http://localhost:8080/api/v1/exit
	This POST request exits the player from the game
	http://localhost:8080/api/v1/enter
	This POST request enters the player into the game. This is the first step of the game.





