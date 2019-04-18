# pyke snake
Battlesnake AI for play.battlesnake.io written in python.

Visit [https://github.com/battlesnakeio/community/blob/master/starter-snakes.md](https://github.com/battlesnakeio/community/blob/master/starter-snakes.md) for API documentation and instructions for running AI.

This AI client uses the [bottle web framework](http://bottlepy.org/docs/dev/index.html) to serve requests and the [gunicorn web server](http://gunicorn.org/) for running bottle on Heroku (if deployed there). Dependencies are listed in [requirements.txt](requirements.txt).

<!-- ## Sample Run of Snake -->



#### Prerequisites

* a working Python 2.7 development environment ([getting started guide](http://hackercodex.com/guide/python-development-environment-on-mac-osx/))
* [pip](https://pip.pypa.io/en/latest/installing.html) to install Python dependencies

## Running the Snake Locally

1) Clone repo to your development environment:

Using SSH
```bash
git clone git@github.com:mroesli/pyke-snake.git
```

Using HTTPS
```bash
git clone https://github.com/mroesli/pyke-snake.git
```

2) Change your directory to pyke-snake:
```bash
cd pyke-snake
```

3) Install dependencies using [pip](https://pip.pypa.io/en/latest/installing.html):
```bash
pip install -r requirements.txt
```

4) Run local server for snake:
```bash
python app/main.py
```

5) After doing the previous step, we will have a snake running on http://localhost:8080 (Check the link for API documentation). We can test if our snake is running by opening up another terminal, and sending a curl to the running snake:
```bash
curl -XPOST -H 'Content-Type: application/json' -d '{ "hello": "world"}' http://localhost:8080/start
```

6) To terminate the snake, go to the terminal running the snake, and stop the process using the following command:
```bash
Ctrl+C
```
## Running the engine

1) Assuming snake is already running locally, open up another terminal.
2) Open up pyke-snake and change your directory to the engine:
```bash
cd engine
```
1) Run the engine using the following:
```bash
./engine dev
```
4) Open up the engine in any browser through this link: http://localhost:3010.
5) You will be presented with a screen to configure the board and also input the link to the running snake.
6) If you followed the previous steps, the snake should be running on https://localhost:8080. Use this as the "Snake URL" and name the snake with whatever name you want.
7) Add as many snakes as possible with known URL's to the game as you want.
8) Click "Start".
9) You should now be able to simulate a game by clicking "play". Have fun!

