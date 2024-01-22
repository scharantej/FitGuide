## Flask Application Design

### HTML Files

1. **index.html**:
   - Serves as the homepage of the application.
   - Includes a form with questions for users to provide information about their fitness level, desired outcomes, and any physical limitations.
   - Contains a button for users to submit their responses to generate their personalized workout plan.

2. **workout_plan.html**:
   - Displays the user's personalized workout plan, including a list of exercises tailored to their needs.
   - Each exercise includes its name, instructional video, modifications, and a checkbox for marking it as completed.
   - Contains a section for users to track their progress and set reminders for their workouts.

3. **progress_report.html**:
   - Provides users with an overview of their progress towards their fitness goals.
   - Displays graphs and charts showcasing their performance over time, including completed workouts, calories burned, and improvements in strength or flexibility.

### Routes

1. **Homepage Route (/)**:
   - Renders the **index.html** page, displaying the form for users to input their information.

2. **Generate Workout Plan Route (/generate_workout_plan)**:
   - Accepts a POST request with the user's responses from the homepage form.
   - Processes the user's information to create a personalized workout plan.
   - Renders the **workout_plan.html** page with the generated workout plan.

3. **Update Progress Route (/update_progress)**:
   - Accepts a POST request with data about the user's completed workouts and other progress metrics.
   - Updates the user's progress in the database.
   - Redirects to the **progress_report.html** page, displaying the updated progress report.

4. **Get Exercise Details Route (/exercise_details)**:
   - Accepts a GET request with an exercise name as a parameter.
   - Fetches detailed information about the exercise, including its instructional video, modifications, and difficulty level.
   - Returns the exercise details in JSON format.

5. **Set Reminder Route (/set_reminder)**:
   - Accepts a POST request with information about the user's desired reminder (e.g., time, date, workout).
   - Schedules a reminder for the user based on the provided information.
   - Returns a success or error message in JSON format.