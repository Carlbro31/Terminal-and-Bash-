# Terminal-and-Bash-
Instructions
Use your command-line skills to uncover the identities of the rogue casino player and dealer colluding to scam Lucky Duck out of thousands of dollars.

After your investigation, you will provide a summary of your findings to the casino.

## Step 1: Investigation Preparation
Your first task is to set up directories to prepare for your investigation.

Begin by making a single directory titled Lucky_Duck_Investigations2.

In this directory, create a directory for this specific investigation titled Roulette_Loss_Investigation2.

In Roulette_Loss_Investigation, create the following directories:

Player_Analysis2 to investigate the casino player.
Dealer_Analysis2 to investigate the dealers.
Player_Dealer_Correlation2 to summarize your findings about the collusion.
Create empty files called Notes_<Directory Name>.txt under each subdirectory to store investigation notes.


  <img width="371" alt="Screenshot 2023-05-29 113821 " src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/71da6166-92aa-47b4-b5a4-b3793a27eb27">
<img width="368" alt="Screenshot 2023-05-29 114821" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/f6373ec5-d261-4a13-8606-9d48dceb8776">

## Step 2: Gathering Evidence
Your next task is to move evidence from the specific days on which Lucky Duck experienced heavy losses at the roulette tables.

Navigate to the directory where you created the Lucky_Duck_Investigations directory and run the following command to set up the evidence files:

wget "https://drive.google.com/uc?id=1ZLY_fuFu3wz7tOlxf-GUrnvp3htuGKSa" -O 3-HW-setup-evidence && chmod +x ./3-HW-setup-evidence && ./3-HW-setup-evidence
After running this command, your current directory should have the following subdirectories:

Dealer_Schedules_0310: Contains the dealer schedules.
Lucky_Duck_Investigations: Contains the investigation directories and notes files you created.
Roulette_Player_WinLoss_0310: Contains the data for player wins and losses.
The Dealer_Schedules_0310 and Roulette_Player_WinLoss_0310 directories contain the dealer schedules and win/loss player data from the roulette tables during the week of March 10.

Since the losses occurred on March 10, 12, and 15, move the schedules for those days into the directory Dealer_Analysis.

Move the files for those days into the directory Player_Analysis.

  <img width="410" alt="Screenshot 2023-05-29 123330" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/648e969d-80e9-4715-9a43-fa491e76f977">
<img width="415" alt="Screenshot 2023-05-29 124354" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/5cc9946e-3b28-42b3-bfdd-bcab6031a08f">

## Step 3: Correlating the Evidence
Your next task is to correlate the large losses from the roulette tables with the dealer schedule. This will help you determine which dealer and player are colluding to steal money from Lucky Duck.

NOTE
Winnings for Lucky Duck Casino are indicated with a positive number and losses are indicated with a negative number.

Complete the player analysis with the following steps:

Navigate to the Player_Analysis2 directory.

Use grep to isolate all of the losses that occurred on March 10, 12, and 15.

Place those results in a file called Roulette_Losses.txt.

Preview the file Roulette_Losses.txt and analyze the data.

Record the following in the Notes_Player_Analysis.txt file:

The times the losses occurred on each day.
Whether there is a certain player who was playing during each of those times.
The total count of times this player was playing. > Hint: Use the wc command to find this value.
Complete the dealer analysis with the following steps:

Navigate to the Dealer_Analysis directory.

This file contains the dealer schedules for the various Lucky Duck casino games: Blackjack, Roulette, and Texas Hold 'Em.

Preview the schedule to view the format and to understand how the data is separated.
Using your findings from the player analysis, create a separate script to look at each day and time that you determined losses occurred. Use awk, pipes, and grep to isolate out the following four fields:

Time

a.m./p.m.

First name of roulette dealer

Last name of roulette dealer

For example, if a loss occurred on March 10 at 2 p.m., you would write one script to find the roulette dealer who was working at that specific day and time. 
Run all of the scripts and append those results to a file called Dealers_working_during_losses.txt.

Preview your file Dealers_working_during_losses.txt, and analyze the data.

Record the following in the Notes_Dealer_Analysis.txt file:

The primary dealer working at the times where losses occurred.

How many times the dealer worked when major losses occurred.

Complete the player/employee correlation.
In the notes file of the Player_Dealer_Correlation directory, add a summary of your findings noting the player and dealer you believe are colluding to scam Lucky Duck.

Make sure to document your specific reasons for this finding.

<img width="476" alt="Screenshot 2023-05-29 131605" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/50797578-17c0-462c-a7a4-7ff02d75d724">
<img width="482" alt="Screenshot 2023-05-29 133114" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/1a56a1c0-e659-4e2e-a35f-b1bae22e480e">
<img width="560" alt="Screenshot 2023-05-29 141020" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/65f5f802-e010-4a18-ba3f-9dbd6d437042">
<img width="482" alt="Screenshot 2023-05-29 133114" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/b464a93b-aecc-4b63-a63f-392a130b7c1d">
<img width="550" alt="Screenshot 2023-05-29 142026" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/feb77435-12df-416d-ab51-6394691535ca">

  
## Step 4: Scripting Your Tasks
You manager is impressed with the work you have done so far on the investigation.

They've now tasked you with building a shell script that can easily analyze future employee schedules. They will use this script to determine which employee was working at a given time in the case of future losses.

Complete the following tasks:

Remain in the Dealer_Analysis directory. Develop a shell script called roulette_dealer_finder_by_time.sh that can analyze the employee schedule to easily find the roulette dealer at a specific time.
Design the shell script to accept the following two arguments:
Date (four digits)
Time
NOTE
The argument should be able to accept a.m. or p.m.

Test your script on the schedules to confirm that it outputs the correct dealer at the time specified.
  
  <img width="550" alt="Screenshot 2023-05-29 142026" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/609f0aee-9223-4615-b11c-948ac918b6cf">
<img width="547" alt="Screenshot 2023-05-29 143754" src="https://github.com/Carlbro31/Terminal-and-Bash-/assets/127357666/a10583b6-02f8-4277-9653-1ff9db895c6e">
