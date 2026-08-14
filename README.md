# GrowMint

A full-stack digital marketing agency website that allows businesses to explore marketing services, create an account, manage their profile, and submit their marketing requirements through a structured client onboarding form.

Built as a **Mini Project for the Web Programming Laboratory** at **K. J. Somaiya School of Engineering, Academic Year 2025–2026**.

---

## About

Many businesses struggle to promote themselves online and often do not have a structured way to communicate their marketing requirements to a digital marketing agency. Communication through calls or emails can become unorganized, and important details may be missed.

**GrowMint** addresses this problem by bringing service information, user authentication, profile management, and a detailed client requirements form together on a single web platform.

The project simulates a real-world digital marketing agency system where users can register, log in, explore available services, manage their information, and submit their business and marketing requirements.

---

## Objectives

* Create a user-friendly digital marketing website.
* Provide information about different digital marketing services.
* Allow users to create and manage their accounts.
* Collect client marketing requirements through a structured form.
* Improve communication between clients and the digital marketing team.
* Simulate a real-world digital marketing agency system.
* Enhance user experience through animations and interactive elements.
* Design a responsive web interface using HTML, CSS, and JavaScript.
* Implement server-side scripting using PHP.
* Integrate database operations using MySQL.

---

## Features

* User Registration and Signup
* Secure Login and Authentication
* User Profile Management
* Digital Marketing Services Section
* Client Onboarding Form
* Business Information Collection
* Marketing Goals and Requirements Collection
* Form Validation
* MySQL Database Integration
* Interactive UI Elements and Animations
* About Us and Contact Us Sections
* Structured storage of client requirements

---

## Tech Stack

| Layer                   | Technology            |
| ----------------------- | --------------------- |
| Front-end               | HTML, CSS, JavaScript |
| Back-end                | PHP                   |
| Database                | MySQL                 |
| Development Environment | XAMPP                 |
| Code Editor             | Visual Studio Code    |

---

## System Flow

```text
             ┌─────────────┐
             │    Home     │
             └──────┬──────┘
                    │
              ┌─────▼─────┐
              │   Signup  │
              └─────┬─────┘
                    │
              ┌─────▼─────┐
              │   Login   │
              └─────┬─────┘
                    │
          ┌─────────▼─────────┐
          │     Services      │
          └─────────┬─────────┘
                    │
        ┌───────────▼───────────┐
        │ Client Details Form   │
        └───────────┬───────────┘
                    │
             ┌──────▼──────┐
             │   MySQL DB  │
             └─────────────┘
```

Users can also access the **About Us**, **Contact Us**, and **Profile** sections throughout the website.

---

## Pages

| Page                    | Description                                                        |
| ----------------------- | ------------------------------------------------------------------ |
| **Home**                | Introduction to GrowMint and navigation to different sections      |
| **Login**               | Allows registered users to authenticate using their credentials    |
| **Signup**              | Allows new company representatives to create an account            |
| **Services**            | Displays the digital marketing services offered                    |
| **About Us**            | Provides information about the company and developers              |
| **Contact Us**          | Displays company contact information                               |
| **Profile**             | Allows users to view and edit their information                    |
| **Client Details Form** | Collects detailed business and marketing requirements from clients |

---

## Main Modules

### 1. User Authentication Module

Handles registration and login functionality.

* New users can create an account.
* Registered users can log in using their credentials.
* User information is stored in the MySQL database.
* Email uniqueness is maintained during registration.

### 2. Services Module

Provides information about the digital marketing services offered by GrowMint.

Users can explore the available services before submitting their requirements.

### 3. Profile Module

Allows registered users to view and update their personal information.

### 4. Client Onboarding Module

Collects detailed information about the client's business and marketing requirements, including:

* Company information
* Industry
* Selected service
* Budget
* Marketing goals
* Target audience
* Business location
* Project timeline
* Additional requirements

### 5. Database Module

MySQL is used to store and manage user and client information.

---

## Database Design

**Database Name:** `DigitalMarketing`

The database consists of two linked tables:

* `user`
* `client`

When a user signs up, their information is stored in the `user` table. Once the user submits their marketing requirements, the corresponding information is stored in the `client` table.

### User Table

| Field      | Type     | Description                   |
| ---------- | -------- | ----------------------------- |
| `user_id`  | INT (PK) | Unique ID for each user       |
| `name`     | VARCHAR  | Name of the user              |
| `email`    | VARCHAR  | Unique email address          |
| `password` | VARCHAR  | User password stored securely |
| `phone`    | INT      | Contact number of the user    |

### Client Details Table

| Field          | Type     | Description                            |
| -------------- | -------- | -------------------------------------- |
| `id`           | INT (PK) | Unique ID assigned to the client entry |
| `company_name` | VARCHAR  | Name of the company                    |
| `website`      | VARCHAR  | Company website                        |
| `industry`     | VARCHAR  | Type of industry                       |
| `service`      | VARCHAR  | Selected marketing service             |
| `budget`       | INT      | Monthly marketing budget               |
| `goals`        | TEXT     | Marketing goals                        |
| `location`     | VARCHAR  | Business location                      |
| `years`        | INT      | Years in business                      |
| `teamSize`     | INT      | Size of the team                       |
| `audience`     | TEXT     | Target audience                        |
| `timeline`     | VARCHAR  | Project deadline                       |
| `requirements` | TEXT     | Detailed client requirements           |

---

## Project Structure

The project is organized into separate files and folders for front-end, back-end, database, styling, scripts, and other resources.

```text
GrowMint/
│
├── HTML / PHP Pages
│   ├── Home
│   ├── Login
│   ├── Signup
│   ├── Services
│   ├── About Us
│   ├── Contact Us
│   ├── Profile
│   └── Client Details
│
├── CSS
│   └── Stylesheets
│
├── JavaScript
│   └── Scripts
│
├── Images
│   └── Website Assets
│
├── Database
│   └── SQL Files
│
└── README.md
```

> The structure above represents the organization of the project. File and folder names can be modified according to the actual repository structure.

---

## Prerequisites

Before running GrowMint, ensure that the following are installed:

* **XAMPP**
* **PHP**
* **MySQL**
* **Web Browser**
* **Visual Studio Code** or another code editor

---

## Installation & Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/Purva1206/GrowMint.git
```

### Step 2: Move the Project

Place the project folder inside the XAMPP `htdocs` directory.

```text
xampp/
└── htdocs/
    └── GrowMint/
```

### Step 3: Start XAMPP

Open XAMPP Control Panel and start:

* Apache
* MySQL

### Step 4: Create the Database

Open **phpMyAdmin** and create a database named:

```text
DigitalMarketing
```

### Step 5: Import Database

Import the project's SQL database file into the `DigitalMarketing` database.

The database should contain:

```text
user
client
```

### Step 6: Configure Database Connection

Update the PHP database connection file with the appropriate MySQL credentials if required.

Typical local configuration:

```text
Host: localhost
Username: root
Password: 
Database: DigitalMarketing
```

### Step 7: Run the Project

Open a web browser and navigate to:

```text
http://localhost/GrowMint/
```

---

## Validation & Security

The project incorporates basic validation and authentication mechanisms to improve the reliability of user input and account management.

These include:

* Required-field validation
* Email validation
* Login authentication
* Unique email checking
* Server-side form processing
* Secure handling of user passwords

---

## Testing

The following test cases can be performed to verify the functionality of the system:

| Test Case                        | Expected Result                        |
| -------------------------------- | -------------------------------------- |
| Register with valid details      | Account should be created              |
| Register with an existing email  | Registration should be rejected        |
| Login with valid credentials     | User should be authenticated           |
| Login with incorrect credentials | Appropriate error should be displayed  |
| Submit incomplete form           | Validation should be triggered         |
| Submit valid client details      | Data should be stored in database      |
| Update profile                   | User information should be updated     |
| Navigate between pages           | Correct page should open               |
| Access services                  | Available services should be displayed |

---

## 🔗 Repository

**GitHub:** https://github.com/Purva1206/GrowMint

---
