1.PYTHON QUIZ

print("****************************************")
print("Welcome to the Python Programming Quiz")

# Define the list of questions with their correct answers
question_bank = [
    {"text": "What is the capital of France?", "answer": "C"},
    {"text": "Which programming language is known for its simplicity and readability?", "answer": "A"},
    {"text": "What is the result of 2 + 3 * 4?", "answer": "D"},
    {"text": "Which of the following is a data type in Python?", "answer": "B"}
]

# Define the options for each question
options = [
    ["A. Berlin", "B. Madrid", "C. Paris", "D. Rome"],
    ["A. Python", "B. Java", "C. C++", "D. Ruby"],
    ["A. 20", "B. 14", "C. 12", "D. 14"],
    ["A. Boolean", "B. List", "C. Function", "D. All of the above"]
]

# Initialize the player's score
score = 0

# Function to check if the user's answer is correct
def check_answer(user_guess, correct_answer):
    if user_guess == correct_answer:
        return True
    else:
        return False

# Loop through each question and present options to the user
for question_num in range(len(question_bank)):
    print("******************************************")
    print(question_bank[question_num]["text"])
    for i in options[question_num]:
        print(i)
    
    guess = input("Enter your answer (A/B/C/D):").upper()
    is_correct = check_answer(guess, question_bank[question_num]["answer"])
    
    if is_correct:
        score += 1
        print("Correct!")
    else:
        print("Incorrect.")
        print(f"The correct answer is {question_bank[question_num]['answer']}")
    
    print(f"Your current score is {score}/{question_num + 1}")

# Display the final score
print("****************************************")
print(f"You have answered {score} out of {len(question_bank)} questions correctly.")
print(f"Your score is {score / len(question_bank) * 100:.2f}%")
print("Thank you for taking the quiz!")
