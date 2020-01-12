# Chess-AI
Created for ICS 4UI - By Huck Kim and Tim Zwart

**Goal**: The goal of this project is to create an artificial intelligence that is able to play a game of chess. This means that it must follow the rules of chess, but also make moves based on a logic system. The method that is being planned on used is a variation of Minimax. It will be able to play as both white and black and represent a point system symbolizing the state of the game and who it considers to be ahead. 

### What it should Accomplish
* Making basic piece moves
* Doing special moves such as castling, en passant, and promotion
* Able to recognize checkmate both receiving and dealing

### Timeline

Basic stages of the project
1.	Research 
2.	Board Representation
3.	Move generation
4.	Move evaluation
5.	Tree Pruning improvement
6.	Calculation improvement
7.	Visuals (if time allows)

### What Are We Doing?
We are creating a Chess AI that is able to play chess. The term “play chess” is used very loosely as a good Chess AI will be much more complex and difficult to create than an AI that has very simple reasoning. There are three major sub groups and ideas that we need to plan and code for our AI to work effectively and efficiently. They are as follows:

* Board Representation
*	Move Searching
*	Move Evaluation

### What Have We Done So Far?

The beginning of a good Chess AI is with the board representation as it is the underlying data structure that the Move Searching and the Move evaluation is based on. We have decided to have a bitboard representation hybrid. This means that the state of the board will be represented as both an 8 x 8 array that we can access, but also as multiple vectors that contain important information such as the where a piece can attack and move. 

### Major Data Structures in our Code
We have two major classes currently,  a Pieces class and a Board class. The Pieces Class contains information that reside in pieces such as what piece it is, what color, where it’s attacking, and where it can move. Some pieces contain other special information such as castling for a king and en passant for a pawn. We have currently coded all the movement, including the special cases. 

### Move Searching
We have already developed some ideas on how we are going to search for moves. Our main idea is to do a breadth first search for 4 ply, which is equivalent to 2 turns, and then do a depth first search on paths that look promising. We are determining this by ordering operations starting from checks, to see if there are any mates, to captures, to see if there is any material advantages that is available, and finally quiet moves, neither checks or captures. 
