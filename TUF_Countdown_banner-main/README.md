# takeUforward: Countdown Banner

This is a hiring assessment for the Software Engineer role at takeuforward.

Here's a comprehensive analysis of the GitHub repository `TUF_Countdown_banner`, covering the technologies utilized and the functionalities provided.

## Overview

The **TUF Countdown Banner** project is a dynamic, single-page website built with React. It features a customizable banner that displays a countdown timer. The banner is managed through an internal dashboard, enabling users to toggle its visibility, update content, set a countdown, and provide a clickable link. The application uses a MySQL database to store the banner settings persistently.

## Technologies Used

### Frontend:
- **React:** A JavaScript library for building user interfaces, used to create the website's dynamic and responsive front end.
- **CSS:** For styling components, delivering a clean and professional UI.
- **Axios:** A promise-based HTTP client for browsers and Node.js, used to interact with the backend API.

### Backend:
- **Node.js:** A JavaScript runtime built on Chrome's V8 engine, used to run the backend server.
- **Express:** A minimal and flexible Node.js web application framework providing a robust set of features to build web and mobile applications.
- **MySQL:** A relational database management system used to store and manage banner settings, such as the description, timer, and link.

### Database:
- **MySQL Database:** Used to store banner-related information, including the description, timer settings, and associated link.

## Functionality

### Banner Display:
- The main feature is a banner at the top of the webpage that includes a countdown timer showing the time remaining before the banner disappears.

### Dashboard Controls:
- **Banner On/Off:** Users can toggle the banner's visibility on the main website through the dashboard.
- **Update Banner Content:** Users can modify the text displayed on the banner.
- **Set Timer:** The dashboard allows users to set a countdown timer, displayed as a reverse clock on the banner.
- **Add a Link:** Users can provide a clickable link on the banner, directing visitors to a specified URL.

### Persistent Storage:
- The banner’s settings, including the description, timer, and link, are stored in a MySQL database, ensuring that the configuration persists across sessions.

### Responsive Design:
- The website is designed to be responsive, ensuring it looks and functions well on various devices, including desktops, tablets, and mobile phones.

## Detailed Workflow

### Initial Setup:
- When the application starts, it retrieves the current banner settings from the MySQL database via the backend API.

### Banner Updates:
- When the user updates the banner settings via the dashboard, the new settings are sent to the backend using an API call (handled by Axios). The backend updates the database with the new settings and returns the updated data to the frontend.

### Real-Time Updates:
- The banner immediately reflects the changes made via the dashboard, such as updating the description, changing the timer, or toggling visibility.

## Key Features

- **Dynamic Banner:** A dynamic banner that updates in real-time based on user inputs from the dashboard.
- **Internal Dashboard:** A fully functional dashboard to control the banner's content, visibility, and behavior.
- **Countdown Timer:** A countdown timer displayed on the banner that can be set and updated via the dashboard.
- **Database Integration:** Persistent storage of the banner's settings using MySQL.
- **Responsive Design:** The application is optimized for various screen sizes.

## Steps to Run the TUF Countdown Banner Project Locally

### Prerequisites
Ensure the following are installed on your system:
- **Node.js** (version 12 or higher)
- **MySQL** (for database management)
- **Git** (optional, for cloning the repository)

### Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/manni2000/TUF_Countdown_banner.git
Install Dependencies:

bash
Copy code
# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
Set Up the MySQL Database:

Open your MySQL client and create a new database for the project:
sql
Copy code
CREATE DATABASE tuf_countdown_banner;
Create the necessary tables in the tuf_countdown_banner database:
sql
Copy code
USE tuf_countdown_banner;

CREATE TABLE banner (
  id INT AUTO_INCREMENT PRIMARY KEY,
  description VARCHAR(255) NOT NULL,
  timer INT NOT NULL,
  link VARCHAR(255) NOT NULL,
  isVisible BOOLEAN NOT NULL
);
Optionally, insert a sample row into the banner table:
sql
Copy code
INSERT INTO banner (description, timer, link, isVisible)
VALUES ('Sample Banner', 3600, 'https://www.example.com', TRUE);
Configure Environment Variables:

Go to the server directory and create a .env file:
bash
Copy code
cd server
touch .env
Add the following content to your .env file:
bash
Copy code
PORT=5000
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=tuf_countdown_banner
Replace your_mysql_username and your_mysql_password with your actual MySQL credentials.
Start the Backend Server:

bash
Copy code
npm start
This will start the backend server on http://localhost:5000.

Start the Frontend Development Server:

bash
Copy code
cd client
npm start
The frontend development server will start on http://localhost:3000.

License
MIT License

© 2024 by Devesh Verma: Do not use without permission.

css
Copy code

This README provides a clear guide to setting up and running the project, as well as an overview of its features and technologies.






