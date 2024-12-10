Interactive Quiz Game Documentation
Project Overview: The Interactive Quiz is a web-based game built using HTML, CSS, and JavaScript, where the user answers a set of questions, with the goal of getting a high score. The game uses an array of objects to store the questions and answers, offering flexibility for future modifications or expansions. The goal of this project is to provide a user-friendly and visually appealing quiz game with real-time interaction and feedback.
________________________________________
Key Features:
1.	Questionnaire Structure:
o	Questions are stored in an array of objects, making the quiz dynamic and flexible.
o	Each object contains the question text, multiple choice options, and the correct answer.
2.	User Interface:
o	Main Game Screen: Displays the current question and multiple-choice answers.
o	Navigation Buttons: Includes a "Next Question" button to proceed through the quiz.
o	Score Display: Shows the current score and the number of questions answered correctly.
o	Responsive Layout: The design is responsive, adjusting to different screen sizes (mobile, tablet, desktop).
3.	User Feedback:
o	At the end of the quiz, the user receives a modal showing:
	Total score (number of correct answers).
	The number of wrong answers.
	A percentage score, which is calculated based on correct answers.
	Remarks or comments based on the score (e.g., "Great job!" or "Try again").
4.	Interactive Modal Windows:
o	Results Modal: Shows the user's score, number of correct/incorrect answers, and grade percentage.
o	Option Modal: Prompts the user if they attempt to move to the next question without selecting an answer.
5.	Timed Features:
o	The quiz introduces a countdown timer (using a simple 10-second delay before the first question appears). This can be used to simulate a timed quiz or add suspense to the gameplay.
________________________________________
Detailed Breakdown of the Project:
1. HTML Structure:
The HTML structure consists of several main sections that contribute to the functionality and user experience.
•	Main Container (<main>): This is the main wrapper for the game UI and contains both the quiz interface and the modals.
•	Modal Containers:
o	Result Modal (id="score-modal"): A modal window that appears when the quiz ends, showing the final score, number of correct answers, and feedback. This modal contains:
	A congratulatory message.
	The number of attempts, correct answers, wrong answers, and the final grade percentage.
	A "Continue" button that closes the modal and optionally allows the user to restart or proceed.
o	Option Modal (id="option-modal"): A smaller modal that informs the player to select an answer if they try to proceed without doing so.
•	Game Quiz Container (<div class="game-quiz-container">): The main section that holds the current quiz question, options, and progress information.
o	Game Details Container: Displays the current score and the current question number.
o	Game Question Container: Shows the text of the current question.
o	Game Options Container: Displays multiple-choice answers (radio buttons), where each answer is clickable.
o	Next Button Container: Contains a button to move to the next question after an answer is selected.
2. CSS Styling:
The CSS focuses on making the quiz visually appealing and responsive. It includes styles for layout, fonts, buttons, and modals.
•	General Layout:
o	The body has a background image with a pink overlay, ensuring that the quiz interface stands out against the background.
o	The .game-quiz-container class defines the width, height, and positioning of the main quiz box. It also uses flexbox to center the content vertically and horizontally.
•	Responsive Design:
o	The media queries adjust the layout for smaller screens, ensuring that the quiz is usable on mobile and tablet devices.
o	Elements such as the question box, answer buttons, and modals resize to fit smaller screen widths.
•	Animations:
o	The @keyframes fadeIn animation smoothly animates the appearance of modals when they are shown.
•	Buttons & Interactions:
o	The buttons and radio button labels are designed with hover effects and animations for smooth transitions.
o	When a radio button is selected, the label changes its background color, providing visual feedback.
3. JavaScript Functionality:
JavaScript is responsible for the interactivity and dynamic behavior of the quiz. The main functionality includes the following:
•	Quiz Data:
o	An array of objects stores the questions, options, and the correct answer for each question.
o	This structure allows easy modification of the quiz content (e.g., adding more questions or changing answer options).
•	Variables:
o	currentQuestionIndex: Tracks the index of the current question.
o	correctAnswers: Stores the number of correct answers selected by the user.
o	totalQuestions: Holds the total number of questions (in this case, 10).
o	score: Stores the user's score based on correct answers.
•	Functions:
o	NextQuestion(index): This function is called on page load and every time the user moves to the next question. It updates the UI with the current question text, answer options, and progress information (score and question number).
o	handleNextQuestion(): This function validates the user's answer and proceeds to the next question. It ensures that an answer is selected before moving on and updates the score if the answer is correct.
o	showResults(): Once all questions are answered, this function calculates the final score, displays the result modal, and provides feedback to the user.
o	closeScoreModal() and closeOptionModal(): These functions close the modals when the user presses the "Continue" button.
4. Game Flow:
1.	Page Load:
o	When the page loads, the first question appears after a brief countdown timer (10 seconds).
2.	Question and Options Display:
o	The current question and its multiple-choice options are displayed. The user must select one of the options.
3.	Answer Submission:
o	Once the user selects an option, they can click the "Next Question" button to proceed.
4.	Option Validation:
o	If the user attempts to move to the next question without selecting an option, a modal will inform them to choose an answer first.
5.	Results:
o	At the end of the quiz, the results modal shows the number of correct answers, the final grade, and a personalized remark.
6.	End of Quiz:
o	The user is shown their final score along with their correct and incorrect answers. The modal offers a "Continue" button to proceed after reviewing the results.
________________________________________
Future Enhancements:
1.	Question Randomization:
o	Implement randomization of questions and answer choices to make each game session unique.
2.	Timer:
o	Add a countdown timer for each question, where the user has a limited time to answer.
3.	User Profiles:
o	Introduce a user authentication system where players can log in to save and track their scores over time.
4.	Expand Question Pool:
o	Increase the number of questions and create categories for different types of quizzes (e.g., Science, History, General Knowledge).
5.	Audio and Visual Effects:
o	Add sound effects for correct/incorrect answers and animations for transitions between questions.
________________________________________
Conclusion:
This Interactive Quiz Game project combines HTML, CSS, and JavaScript to create a fun and engaging user experience. The modular approach to storing quiz data allows for easy updates and modifications, making this a scalable and versatile project. The responsive design ensures that the game is accessible on various devices, while the dynamic user interface provides instant feedback to the player. This documentation serves as a comprehensive guide to the project's structure, design, and functionality.

