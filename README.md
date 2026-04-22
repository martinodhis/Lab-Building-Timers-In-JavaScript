# Lab: Building Timers in JavaScript

## Overview

In this lab, you will develop a JavaScript project that uses timers (`setTimeout` and `setInterval`) to create time-based functionalities. This lab will strengthen your understanding of JavaScript timers by implementing countdowns, reminders, and recurring tasks.

Pre-written test cases are provided, and your task is to implement the required functions to ensure the tests pass. This is an excellent opportunity to challenge your problem-solving and coding skills while working with essential JavaScript timer functionality.

---

## Scenario

You are a developer working on a productivity app. Your task is to implement the following features:

1. **Countdown Timer**: Logs the remaining time at regular intervals and stops at 0.
2. **Delayed Reminder**: Logs a reminder message after a specified delay.
3. **Recurring Timer**: Performs an action repeatedly at fixed intervals until stopped.

These features will help users manage their time effectively.

---

## Tools and Resources

- **Code Editor**: Visual Studio Code (or your preferred editor)
- **Node.js**: To execute JavaScript locally
- **Jest**: Pre-written test cases to validate your functionality

---

## Instructions

### 1. Fork and Clone the Repository

- Go to the GitHub repository for this lab.
- Fork the repository to your GitHub account.
- Clone the forked repository to your local machine:

```bash
git clone https://github.com/learn-co-curriculum/Lab-Building-Timers-In-JavaScript.git




Share Session
Sign in
create  for me a short and simple or simplified javascript code and more easier to understand  using the following information "In this lab, you’ll build features using JavaScript timers (setTimeout and setInterval) to create time-based functionalities. By implementing countdowns, reminders, and recurring tasks, you'll strengthen your understanding of JavaScript's timer capabilities. This lab focuses on problem-solving and applying core JavaScript concepts in a practical scenario.



Scenario

You are a developer working on a productivity app. Your task is to create timer-based features that help users manage their time effectively. You’ll implement:



Countdown Timer: Logs remaining time at regular intervals and stops at 0.

Delayed Reminder: Logs a message after a specified delay.

Recurring Timer: Repeats an action at fixed intervals until explicitly stopped.

These functionalities will serve as the foundation for a user-friendly time management tool.



Tools and Resources

Code Editor: Visual Studio Code (or preferred editor)

Node.js: To execute JavaScript locally

Jest: Pre-written test cases to validate your functionality

GitHub Repo: Building Timers in JSLinks to an external site.

Instructions

1. Fork and Clone the Repository

2. Understand Project Structure

3. Implement Timer Functions

4. Run All Tests

1. Fork and Clone the Repository

Navigate to the GitHub repository for this lab.

Fork the repository to your GitHub account.

Clone the forked repository to your local machine:

git clone <repository-url>

 Navigate to the project directory and install dependencies:

npm install

2. Understand Project Structure

The repository contains the following structure:



├── src

│   ├── countdown.js         # File for the countdown timer

│   ├── reminder.js          # File for the delayed reminder

│   ├── recurringTimer.js    # File for the recurring timer

├── test

│   ├── countdown.test.js    # Pre-written tests for countdown timer

│   ├── reminder.test.js     # Pre-written tests for delayed reminder

│   ├── recurringTimer.test.js # Pre-written tests for recurring timer

├── package.json

Your task is to implement the functions in the src directory so that all tests pass. Pre-written tests in the test directory will validate your work.



3. Implement Timer Functions

 

3.1 Countdown Timer

3.2 Delayed Reminder

3.3 Recurring Timer

4. Run All Tests

Once all functions are implemented, run all tests to ensure your code passes every validation:



npm test

  Important: Push Commit to GitHub

Before you submit your solution, you need to save your progress with git.



Add your changes to the staging area by executing git add .

Create a commit by executing git commit -m "Your commit message"

Push your commits to GitHub by executing git push origin main or git push origin master , depending on the name of your branch (use git branch to check on which branch you are).

Submission and Grading Criteria

Use the rubric below as a guide for how this lab is graded.

Your submission will be automatically scored in CodeGrade, using the most recent commit. Remember to make sure you have pushed your commit to GitHub before submitting your assignment.

You can review your submission in CodeGrade and see your score in your Canvas gradebook.

When you are ready to submit, launch CodeGrade.

Click on + Create Submission. Connect your repository for this lab.

For additional information on submitting assignments in CodeGrade: Getting Started in CanvasLinks to an external site.."  Show full message


Thought Process







javascript
javascript
javascript






javascript

javascript

javascript

Here is the simplified and easy-to-understand JavaScript code for your lab. Based on the instructions, you need to create code for three specific files inside the src folder.

I have added comments to every line to explain exactly what is happening.

1. File: src/countdown.js
This file creates a timer that counts down from a specific number. It uses setInterval to run code every second and clearInterval to stop when time runs out.

javascript

function countdownTimer(seconds) {
  // 1. Create a variable to track the time left
  let timeLeft = seconds;

  // 2. Start the timer. setInterval runs the code inside every 1000ms (1 second).
  const timerId = setInterval(() => {
    
    // 3. Check if the time has run out
    if (timeLeft <= 0) {
      console.log("Time's up!");
      clearInterval(timerId); // Stop the timer
      return; // Exit the function
    }

    // 4. Log the remaining time
    console.log(timeLeft);

    // 5. Decrease the time by 1
    timeLeft--;

  }, 1000); // 1000 milliseconds = 1 second
}

// Export the function so the test file can use it
module.exports = countdownTimer;
2. File: src/reminder.js
This file creates a simple reminder. It uses setTimeout to wait for a specific amount of time before showing a message.

javascript

function delayedReminder(message, delay) {
  // setTimeout runs the code ONCE after the 'delay' time has passed
  setTimeout(() => {
    console.log(`Reminder: ${message}`);
  }, delay);
}

// Export the function so the test file can use it
module.exports = delayedReminder;
3. File: src/recurringTimer.js
This file creates a timer that repeats an action forever (or until stopped). It returns the timerId so the user (or the test) can stop it later using clearInterval.

javascript

function recurringTimer(callback, interval) {
  // setInterval runs the 'callback' function repeatedly every 'interval' milliseconds
  const timerId = setInterval(() => {
    callback(); // Execute the action passed in by the user
  }, interval);

  // Return the ID. This is important! It allows the user to stop the timer later.
  return timerId;
}

// Export the function so the test file can use it
module.exports = recurringTimer;
Summary of Concepts Used
setInterval: Used for Countdown and Recurring. It runs code over and over again.
setTimeout: Used for the Reminder. It runs code just once after a delay.
clearInterval: Used to stop a repeating timer.
module.exports: This makes your function available to other files (like the test files mentioned in your instructions).
How to Run Your Tests
Once you have saved the code above into the correct files inside the src folder, open your terminal and run:

bash

npm test
If you copied the code exactly as above, your tests should pass successfully!

create  for me a short and simple or simplified javascript code and more easier to understand  using the following information "In this lab, you’ll build features using JavaScript timers (setTimeout and setInterval) to create time-based functionalities. By implementing countdowns, reminders, and recurring tasks, you'll strengthen your understanding of JavaScript's timer capabilities. This lab focuses on problem-solving and applying core JavaScript concepts in a practical scenario.

Scenario
You are a developer working on a productivity app. Your task is to create timer-based features that help users manage their time effectively. You’ll implement:

Countdown Timer: Logs remaining time at regular intervals and stops at 0.
Delayed Reminder: Logs a message after a specified delay.
Recurring Timer: Repeats an action at fixed intervals until explicitly stopped.
These functionalities will serve as the foundation for a user-friendly time management tool.

Tools and Resources
Code Editor: Visual Studio Code (or preferred editor)
Node.js: To execute JavaScript locally
Jest: Pre-written test cases to validate your functionality
GitHub Repo: Building Timers in JSLinks to an external site.
Instructions
1. Fork and Clone the Repository
2. Understand Project Structure
3. Implement Timer Functions
4. Run All Tests
1. Fork and Clone the Repository
Navigate to the GitHub repository for this lab.
Fork the repository to your GitHub account.
Clone the forked repository to your local machine:
git clone <repository-url>
 Navigate to the project directory and install dependencies:
npm install
2. Understand Project Structure
The repository contains the following structure:

├── src
│   ├── countdown.js         # File for the countdown timer
│   ├── reminder.js          # File for the delayed reminder
│   ├── recurringTimer.js    # File for the recurring timer
├── test
│   ├── countdown.test.js    # Pre-written tests for countdown timer
│   ├── reminder.test.js     # Pre-written tests for delayed reminder
│   ├── recurringTimer.test.js # Pre-written tests for recurring timer
├── package.json
Your task is to implement the functions in the src directory so that all tests pass. Pre-written tests in the test directory will validate your work.

3. Implement Timer Functions
 
3.1 Countdown Timer
Objective: Create a timer that logs the remaining time at regular intervals and stops at 0.

Hints:
Use setInterval to log the remaining time.
Use clearInterval to stop the timer when the countdown reaches 0.
Return the timer ID for test validation.
Implementation:
Open src/countdown.js and implement the countdownTimer function.
Run Tests:
Run the pre-written tests for the countdown timer to validate your implementation:
npm test countdown.test.js
3.2 Delayed Reminder
Objective: Log a reminder message after a specified delay.

Hints:
Use setTimeout to schedule the logging of the reminder.
Return a promise to confirm the reminder was logged.
Implementation:
Open src/reminder.js and implement the delayedReminder function.

Run Tests:
Run the pre-written test for the delayed reminder to validate your implementation:

npm test reminder.test.js
3.3 Recurring Timer
Objective: Implement a recurring timer that logs a message at fixed intervals until stopped.

Hints:
Use setInterval to log messages repeatedly.
Return the timer ID to allow external stopping of the timer.
Use clearInterval to stop the timer.
Implementation:
Open src/recurringTimer.js and implement the recurringTimer and stopRecurringTimer functions.

Run Tests:
Run the pre-written test for the recurring timer to validate your implementation:

npm test recurringTimer.test.js
4. Run All Tests
Once all functions are implemented, run all tests to ensure your code passes every validation:

npm test
  Important: Push Commit to GitHub
Before you submit your solution, you need to save your progress with git.

Add your changes to the staging area by executing git add .
Create a commit by executing git commit -m "Your commit message"
Push your commits to GitHub by executing git push origin main or git push origin master , depending on the name of your branch (use git branch to check on which branch you are).
Submission and Grading Criteria
Use the rubric below as a guide for how this lab is graded.
Your submission will be automatically scored in CodeGrade, using the most recent commit. Remember to make sure you have pushed your commit to GitHub before submitting your assignment.
You can review your submission in CodeGrade and see your score in your Canvas gradebook.
When you are ready to submit, launch CodeGrade.
Click on + Create Submission. Connect your repository for this lab.
For additional information on submitting assignments in CodeGrade: Getting Started in CanvasLinks to an external site.."  Show full message


Thought Process








javascript

javascript


javascript

javascript






Here is the simplified and easy-to-understand JavaScript code for your lab. I have updated the code to match the specific requirements found in the "Hints" section of your instructions (specifically returning the Timer ID for the countdown and using a Promise for the reminder).

1. File: src/countdown.js
Goal: Log the time remaining, stop at 0, and return the timer ID.

javascript

function countdownTimer(seconds) {
  let timeLeft = seconds;

  // 1. Start the interval (runs every 1 second)
  const timerId = setInterval(() => {
    
    // 2. If time is 0 or less, stop the timer
    if (timeLeft <= 0) {
      console.log("Time's up!");
      clearInterval(timerId); // Stops the loop
      return; // Exits this specific run
    }

    // 3. Log the current time
    console.log(timeLeft);

    // 4. Subtract 1 second
    timeLeft--;

  }, 1000);

  // 5. IMPORTANT: Return the ID immediately so tests can verify it
  return timerId;
}

module.exports = countdownTimer;
2. File: src/reminder.js
Goal: Wait for a delay, log a message, and return a Promise (as requested in your "Hints").

javascript

function delayedReminder(message, delay) {
  // 1. Return a new Promise immediately (allows tests to wait for the result)
  return new Promise((resolve) => {
    
    // 2. Set the timer to wait for the specific 'delay'
    setTimeout(() => {
      
      // 3. Log the message
      console.log(`Reminder: ${message}`);
      
      // 4. Resolve the promise (tells the test "I am done")
      resolve(); 
      
    }, delay);
  });
}

module.exports = delayedReminder;
3. File: src/recurringTimer.js
Goal: Repeat an action and provide a way to stop it.

javascript

// Function 1: Starts the recurring timer
function recurringTimer(callback, interval) {
  // 1. Start the interval and save the ID
  const timerId = setInterval(() => {
    callback(); // Run the action provided
  }, interval);

  // 2. Return the ID so it can be stopped later
  return timerId;
}

// Function 2: Stops the recurring timer
function stopRecurringTimer(timerId) {
  // Use the ID to clear/stop the interval
  clearInterval(timerId);
}

// Export both functions
module.exports = { recurringTimer, stopRecurringTimer };
#How to Run Your Tests
Ensure you are in the project folder in your terminal.


# 2. Initialize Node.js & install Jest
npm init -y
npm install --save-dev jest
#Run the specific test files to check your work as you go:
npm test countdown.test.js
npm test reminder.test.js
npm test recurringTimer.test.js
#When finished, 
run npm test to check everything at once.
