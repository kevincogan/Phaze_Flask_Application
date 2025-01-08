# Flask Dashboard Application

## Overview

This repository contains a Flask-based web application designed to manage user accounts and display personalized dashboards. Users can register, log in, and delete their accounts while accessing dynamic data retrieved from a Flask API server hosted on AWS Elastic Beanstalk.

## Features

1. **User Registration**:
   - Allows users to create an account with a username and password.
   - Interacts with an API to store user data securely.

2. **User Login**:
   - Authenticates users using their credentials.
   - Retrieves and displays personalized data such as activity, calories, and meal information.

3. **Dashboard Display**:
   - Presents dynamic data including daily activity, calorie consumption, and macronutrient breakdown (carbs, protein, fat).
   - Displays meal information categorized by breakfast, lunch, dinner, and snacks.

4. **Account Deletion**:
   - Enables users to delete their accounts securely.

5. **Error Handling**:
   - Handles invalid login, registration, or deletion attempts gracefully with appropriate error messages.

## Prerequisites

- Python 3.x
- Flask (`pip install flask`)
- Requests library (`pip install requests`)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kevincogan/flask-dashboard.git
   cd flask-dashboard
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   ```bash
   python app.py
   ```

4. **Access the Application**:
   Open your browser and navigate to `http://localhost:8082`.

## API Endpoints

### 1. `/` (Home Page)
- Displays the homepage with options to register, log in, or delete an account.

### 2. `/web_register` (Registration Page)
- Handles user registration via POST requests.
- Redirects to the user dashboard upon successful registration.

### 3. `/web_login` (Login Page)
- Authenticates user credentials via POST requests.
- Displays user dashboard with personalized data.

### 4. `/web_delete` (Account Deletion Page)
- Deletes user accounts securely via POST requests.
- Redirects to a success or error page based on the outcome.

## Dynamic Data Retrieval

The application fetches user-specific data from an external API hosted on AWS Elastic Beanstalk. It retrieves:
- Activity level
- Calorie consumption
- Macronutrient breakdown (carbs, protein, fat)
- Meal information (breakfast, lunch, dinner, snacks)

The data is processed and displayed on the user dashboard.

## Templates

- **`index.html`**: Home page template.
- **`register.html`**: Registration form.
- **`login.html`**: Login form.
- **`user.html`**: User dashboard template.
- **`delete_page.html`**: Account deletion form.
- **`error_register.html`**: Registration error page.
- **`error_login.html`**: Login error page.
- **`delete_page_success.html`**: Account deletion success page.
- **`error_delete_account.html`**: Account deletion error page.

## Error Handling

The application displays user-friendly error messages for:
- Failed registration (e.g., username already exists).
- Incorrect login credentials.
- Invalid account deletion attempts.

## Deployment

To deploy this application to a production environment:
1. Set up an EC2 instance or a cloud service (e.g., AWS Elastic Beanstalk).
2. Configure the environment variables and update the API URLs as needed.
3. Run the application in production mode:
   ```bash
   python app.py
   ```

## Contribution

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Commit your changes and push them to your fork.
4. Open a pull request describing your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

Enhance user engagement with this feature-rich Flask Dashboard Application!

