
Bowling Challenge
=================

![alt text](https://github.com/ajitsy/bowling-challenge/blob/master/images/screenshot.png)

Task:
-------
Count and sum the scores of a bowling game for one player (in JavaScript).

How to Use:
-------

Clone the repository

```
$ git clone https://github.com/ajitsy/bowling-challenge.git
```

Open Bowling.html in your preferred browser

```
$ open Bowling.html
```

Run Jasmine to see all tests pass:

```
$ open SpecRunner.html
```

Technologies Used:
-------
* Javascript
* Jasmine
* JQuery

Tests:
-------

```
Scorecard
    can see scores but no totals
        cannot score more than 10 points for first roll
        cannot score more than 10 points for second roll
        cannot score more than 10 points for third roll
        cannot score more than 10 points based on two rolls
        should allow only 10 frames
        cannot use 3rd roll for 10th frame if no strike/spare in frame 10
    can calculate frame total
        shows the frame score
        shows the frame score as NaN when pending a roll due to a spare
        adds additional bonus points for spares and shows score
        adds additional bonus points for a strike and shows score
        adds additional bonus points for two consecutive strikes and shows score
        adds additional bonus points for spares and followed by a strike and shows score
        should take total frame 9 to 30 if frame 9 and subsequent 2 rolls are strikes
        calculates 10th frame total
            gives a total of 30 if player has 3 consecutive strikes
            calculates correct total if player has no strike or spare
            calculates correct total if player has a spare
            calculates correct total if player has a spare & a strike(on 3rd roll)
    calculates running total
        running total starts at zero
        collates frame totals within running total
        returns the running total value
        does not update running total if expecting a bonus roll
        rolls the following: 1,3,1,9,10,0 and expect running score of 24
        rolls 3 consecutive strikes and a spare & expects running score of 40
        expects to score 300 for perfect game

24 specs, 0 failures
```
