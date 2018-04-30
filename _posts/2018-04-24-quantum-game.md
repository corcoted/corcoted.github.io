---
layout: post
title: Quantum State Guessing Game
category: teaching
tags: quantum mechanics, quantum game
date: 2018-04-24
excerpt: >-
  For a couple of years I've been polishing up a classroom activity to demonstrate how quantum measurements work on a simple qubit system.  Here I'd like to summarize the game in simple terms for non-experts.
---
{:gametable: style="display: block; margin-left: auto; margin-right: auto; width: 40%; text-align: center;"}

For a couple of years I've been polishing up a classroom activity to demonstrate how quantum measurements work on a simple qubit system.
The work has just been accepted to *American Journal of Physics* and will appear there later this year.
In the meantime I've pushed the paper onto [arXiv](http://arxiv.org/abs/1804.08417).
Here I'd like to summarize the game in simple terms for non-experts.

## What's a qubit?

Quantum computers typically store data in what are called "quantum bits" or "qubits."
A classical bit is a piece of information that can have two possible values, traditionally called 0 and 1.
Qubits can similarly be either 0 or 1, but can also be superpositions of these two states.
For example, the state could be half 0 and half 1, or one quarter 0 and three-quarters 1.
(For experts, I'm ignoring normalization here for the sake of simplicity.)
Or the proportions can even take values that are complex numbers, half 0 and &radic;-1 halves of 1.

At the end of every quantum computing algorithm, we need to read out the qubits as classical information: back to plain 0's and 1's.
Depending on the proportions of 0 and 1 in the quantum state, we get a random chance of reading 0 or 1 when we do this conversion.
Naturally, this final readout step loses information.
We can recapture the information by repeating the calculation many times and building up statistics of the classical 0's and 1's from the readout step.
To complicate matters more, there are an infinite number of ways to readout the state, and they give different, but related, results.
With enough data of enough types of readings, we can say what the actual quantum state was at the end of the calculation, to within some statistical uncertainty.

Our game simulates this readout process. The players must use the data they collect to determine the actual state of the qubit.
I won't go into the theory here, but it's laid out in full in the [paper](http://arxiv.org/abs/1804.08417).
Here I'll describe how to play the game.

## The Game
### Setup
To play the game you need:

1. Two players, called "The Experiment" and "The Scientist" (two human players is the most fun, but I'm polishing up some code for computer players).
2. A pre-generated Game Table containing the quantum states and measurement probabilities (examples below).
3. A classical random number generator.  My favorite is a 20-sided die (d20).

The playing field for the game is a set of quantum states (A, B, C,...) and three possible measurements (X, Y, and Z).
For each combination of state and measurement there is a probability of reading out a 1 and the complementary probability of reading out a 0.
This information is summarized in the Game Table:

<table class="gametable">
 <tr>
 <th></th><th colspan="4">Measurement probabilites</th>
 </tr>
 <tr>
 <th>States</th><th>Outcome</th><th>X</th><th>Y</th><th>Z</th>
 </tr>
 <tr>
 <th rowspan="2">A</th><td>1</td><td>100%</td><td>50%</td><td>50%</td>
 </tr>
 <tr>
   <td>0</td><td>0%</td><td>50%</td><td>50%</td>
 </tr>
 <tr>
 <th rowspan="2">B</th><td>1</td><td>0%</td><td>50%</td><td>50%</td>
 </tr>
 <tr>
   <td>0</td><td>100%</td><td>50%</td><td>50%</td>
 </tr>
 <tr>
 <th rowspan="2">C</th><td>1</td><td>50%</td><td>100%</td><td>50%</td>
 </tr>
 <tr>
   <td>0</td><td>50%</td><td>0%</td><td>50%</td>
 </tr>
 <tr>
 <th rowspan="2">D</th><td>1</td><td>50%</td><td>0%</td><td>50%</td>
 </tr>
 <tr>
   <td>0</td><td>50%</td><td>100%</td><td>50%</td>
 </tr>
  <tr>
 <th rowspan="2">E</th><td>1</td><td>50%</td><td>50%</td><td>100%</td>
 </tr>
 <tr>
   <td>0</td><td>50%</td><td>50%</td><td>0%</td>
 </tr>
 <tr>
 <th rowspan="2">F</th><td>1</td><td>50%</td><td>50%</td><td>0%</td>
 </tr>
 <tr>
   <td>0</td><td>50%</td><td>50%</td><td>100%</td>
 </tr>
</table>{:gametable}


The above table lists all the combinations of states, measurements, and outcomes.
Let's simplify the table a little by changing the probabilities into die roll ranges for our d20.
Also, since we only have two possible outcomes, 0 or 1, I'll only list the die rolls that represent a measurement of 1.

<table class="gametable">
 <tr>
 <th></th><th colspan="4">Measurement probabilites</th>
 </tr>
 <tr>
 <th>States</th><th>Outcome</th><th>X</th><th>Y</th><th>Z</th>
 </tr>
 <tr>
 <th>A</th><td>1</td><td>1-20</td><td>1-10</td><td>1-10</td>
 </tr>
 <tr>
 <th>B</th><td>1</td><td>none</td><td>1-10</td><td>1-10</td>
 </tr>
 <tr>
 <th >C</th><td>1</td><td>1-10</td><td>1-20</td><td>1-10</td>
 </tr>
 <tr>
 <th >D</th><td>1</td><td>1-10</td><td>none</td><td>1-10</td>
 </tr>
  <tr>
 <th>E</th><td>1</td><td>1-10</td><td>1-10</td><td>1-20</td>
 </tr>
 <tr>
 <th>F</th><td>1</td><td>1-10</td><td>1-10</td><td>none</td>
 </tr>
</table>{:gametable}

Great!  This simplified table is the one we'll use for playing the game.

### Game Rules

Once we have a Game Table and our players, here is how the game goes.

1. The Experiment player secretly chooses a state from the Table (e.g. state "D").
2. The Scientist player requests a measurement X, Y, or Z.
3. The Experiment secretly rolls the d20 and consults the Table by looking at the 
row of the secret state and the column of the measurement.
If the value of the die falls within the range shown on the table entry, then the Experiment reports a result of "one."
Otherwise, the Experiment reports a result of "zero."
4. Now the Scientist has two choices:
    * Guess the state based on the data collected.  A correct guess ends the round but an incorrect guess results in a penalty.
    * Collect more data by going back to Step 2 and asking for another measurement (may be the same as before or different).

Once the Scientist guesses the secret state correctly, the round ends.
The Scientist's score for this round is the number of measurements performed plus a 5 point penalty for each incorrect guess.
Like golf, a lower score is better.

Now the players swap roles and begin a new round.  After a predetermined number of rounds (3 rounds in each role is a good number), the player with the lowest total score wins!

## What does it all mean?

The game demonstrates a few important properties of quantum measurements.
First, the measurement process is inherently random.
This is not a defect of the measurement, but a fundamental property of quantum mechanics.
Second, although the measurement is random, there are some combinations of measurements and states that give the same result every time.
When this happens, we say the state is an "eigenstate" of the measurement with an "eigenvalue" equal to the measurement result.
For example, in the Game Table above state A is an eigenstate of measurement X with corresponding eigenvalue 1,
and state B is also an eigenstate of measurement X, but with eigenvalue 0.
Eigenstates are special indeed:
knowing the eigenstates and eigenvalues of a measurement lets us calculate the measurement probabilities of every other state.
Third, with the exception of eigenstates, we can never be 100% sure of what the secret state is.
The best we can do is take a lot of data and reduce our uncertainty.
This means that there is always a gamble associated with guessing the state (again, except for eigenstates).


One of the difficulties is interpreting the data in a quantitative way.
Guessing the state based on "intuition" is good enough for human players, but for a computer to play the Scientist role it must be able to turn hunches into numbers and evaluate them.
This is pretty straightforward using tools of statistical estimation, but there are a couple of twists.
On the other hand, a suprisingly hard task for the computer is knowing which measurements maximize the amount of new information gained.
I'll discuss these ideas in a later post and perhaps a paper.

There are a lot of other goodies about quantum mechanics hidden in the game, but these are the key points to get you started.
Try it out, and then take a look at the [paper](http://arxiv.org/abs/1804.08417) for some other Game Tables (without eigenstates!) and the theory behind it all.

Enjoy, and happy state hunting!