---
title: "Create a Simple Blackjack Game with HTML and JavaScript"
date: 2024-10-11
categories: [Web Development]
tags: [HTML, JavaScript, Tailwind CSS]
author: Nancy Jiwono
layout: post
description: "Learn how to create a simple Blackjack game using HTML, Tailwind CSS, and JavaScript."
image: /assets/blackJack/coverblackjack.jpeg
comments: true
---

## 📖 Project Overview
This project is a web-based Blackjack game designed to provide an interactive card-playing experience through a browser. Blackjack is a popular card game where players compete against the dealer to get a card value as close as possible to 21 without exceeding it.  

### Key Features:
- Players start with an initial balance (e.g., $5000).  
- Players place bets before starting the game.  
- Players can choose to **Hit** (draw a card) or **Stand** (stop drawing cards).  
- The dealer plays according to standard rules (must draw cards until reaching a minimum value of 17).  
- The winner is determined based on the card values of both the player and the dealer.  

## Project Objectives
The objective of this project is to create a web-based Blackjack simulation as a means of learning programming logic, developing an interactive user interface, and providing simple entertainment. This project also helps in practicing the use of **HTML, Tailwind CSS, and JavaScript** to build a web application.

## Main Features
Here are the key features included in this project:  
#### 1. **User Interface (UI):**  
- Responsive design using **Tailwind CSS**.  
- Players start with an initial balance of **$5000**.  
- Input field to enter the bet amount (minimum **$100**).  
- Visualization of player and dealer cards using card images.  

#### 2. **Game Logic:**  
- Players can choose **Hit** to draw a card or **Stand** to stop drawing cards.  
- The dealer automatically draws cards until reaching a minimum value of **17**.  
- Winner determination based on the card values of the player and the dealer:  
  - The **player wins** if their card value is higher than the dealer’s without exceeding **21**.  
  - The **dealer wins** if their card value is higher than the player’s or if the player **busts** (exceeds **21**).  
  - A **push (tie)** occurs if both the player and dealer have the same card value.  

#### 3. **Betting Features:**  
- Players can place bets before starting the game.  
- The player's balance is updated based on the game result:  
  - **Winning** increases the balance based on the bet amount.  
  - **Losing** decreases the balance based on the bet amount.  
  - If the balance runs out, the game displays a **Game Over** message.  

#### 4. 🃏 **Card Images:**  
- Card images are retrieved from the **images** folder to visually display the player’s and dealer’s cards.  

#### 5. **Additional Features:**  
- Players can continue playing after completing a round.  
- Players can **restart** the game with the initial balance if their balance runs out.

## 🛠️ Technologies Used
This project is built using the following technologies:  
1. **HTML**: For structuring the web page.  
2. **CSS (Tailwind CSS)**: For styling and responsive design.  
3. **JavaScript**: For game logic, user interaction, and DOM manipulation.  
4. **Card Images**: Card image files are stored in the **images** folder and used for visual representation of the cards.  

## 🚀 How to Run the Project
To run this project locally, follow these steps:  
#### 1. **Environment Setup:**  
- Make sure you have a text editor like **Visual Studio Code**.  
- Install the **Live Server** extension in Visual Studio Code.  

#### 2. **Running the Project:**  
- Open the project folder in **Visual Studio Code**.  
- Right-click on the **index.html** file and select **Open with Live Server**.  
- The game will open in your browser.  

#### 3. **Starting the Game:**  
- Enter the **bet amount** and click the button to start the game.

## 🎮 Game Flow
### Example of Game Start  
Here is an example of how the game looks when it starts:  
![Game Start Example](/assets/blackJack/play.png)  

Here is an example of how the game looks when it win:  
![Game Win Example](/assets/blackJack/win.png)  
*This is the initial screen where the player can see their balance, enter a bet amount, and start the game.* 

Here is the detailed game flow:  
#### 1. **Starting the Game:**  
- The player starts with an initial balance of **$5000**.  
- The player enters a **bet amount** (minimum **$100**).  

#### 2. **Card Dealing:**  
- Both the player and the dealer receive **two cards**.  
- One of the dealer’s cards is **face down**.  

#### 3. **Player’s Turn:**  
- The player can choose **Hit** to draw an additional card.  
- The player can choose **Stand** to stop drawing cards.  

#### 4. **Dealer’s Turn:**  
- The dealer automatically draws cards until reaching a minimum value of **17**.  

#### 5. **Determining the Winner:**  
- The player’s and dealer’s card values are compared to determine the winner.  
- **If the player wins**, their balance increases based on the bet amount.  
- **If the player loses**, their balance decreases based on the bet amount.  

#### 6. **Continuing the Game:**  
- The player can proceed to the **next round** or restart the game if their balance runs out.

## 🎉 Conclusion  
This project demonstrates how to create a simple yet visually appealing Blackjack game using **HTML**, **Tailwind CSS**, and **JavaScript**. By incorporating features like responsive design, animations, and interactive elements, the game provides an engaging user experience.  

For the complete source code, visit the [GitHub](https://github.com/nancyjwn/Blackjack-Game).

---
Hope you enjoyed and learned something new! 🎉 

Stay healthy and take care! 💪🏻

Thank youu!!! 