# Discussion Forum System

## Accessing the SSH Key

Before you can clone the repository, you'll need to set up an SSH key for authentication. Follow these steps to generate and add your SSH key to GitHub:

### 1. **Generate an SSH Key (if you don’t have one)**

If you haven't already generated an SSH key, you can do so by following these steps:

#### For Linux/macOS/Windows (Git Bash):
Open your terminal (or Git Bash) and ruQn the following command to generate an SSH key:

```bash
ssh-keygen -t ed25519 -C "anayshirolkar@gmail.com"
```

For older systems that do not support Ed25519, use the RSA option:

```bash
ssh-keygen -t rsa -b 4096 -C "anayshirolkar@gmail.com"
```

#### For Windows (via Git Bash):
If you're using Git Bash on Windows, the process remains the same.

### 2. **Add the SSH Key to GitHub**

Once the SSH key is generated, you need to add the public key to GitHub.

- Copy the public key to your clipboard by running:
  ```bash
  cat ~/.ssh/id_ed25519.pub
  ```
  Or, if you’re using RSA:
  ```bash
  cat ~/.ssh/id_rsa.pub
  ```

- Log into your GitHub account, go to **Settings**, then **SSH and GPG keys**.
- Click **New SSH key**, paste the copied public key into the field, and give it a descriptive title.
- Click **Add SSH key** to save.

### 3. **Clone the Repository Using SSH**

Once your SSH key is added to GitHub, you can securely clone the repository. Use the following command to clone the repository:

```bash
git clone git@github.com:<username>/<repository-name>.git
```

Replace `<username>` with your GitHub username and `<repository-name>` with the repository’s name.

---

## Overview

This project is a **Discussion Forum System** designed to allow users to post questions, provide answers, and search through discussions effectively. The project includes several essential features:

- **UML-Based Class Structure:** Implemented to enhance organization and relationships between questions and answers.
- **Input Validation & Error Handling:** Prevents invalid data entries, ensuring smooth user experience.
- **Enhanced Search Functionality:** Allows users to find relevant discussions quickly.
- **CRUD Operations with Database Integration:** Persistent storage and management of questions and answers.
- **Optimized Codebase:** Improved efficiency and readability, with enhanced documentation.
- **Comprehensive Unit Testing:** Ensures reliable performance of key features.
- **JavaFX UI Integration:** Provides a clean and user-friendly interface for interactions.

## Prerequisites

Before you begin running the project, ensure that you have the following installed:

- **Java Development Kit (JDK)** version 11 or later.
- **JavaFX SDK** (Ensure it's properly configured in your IDE).
- An **Integrated Development Environment (IDE)** such as **IntelliJ IDEA** or **Eclipse**.
- A **Database System** (e.g., MySQL) to handle data persistence.

## Cloning the Repository

To access the project, clone the repository using **SSH** by following these steps:

1. **Generate an SSH Key** (if you haven't already).
2. **Add the SSH Key to GitHub**.
3. **Clone the Repository Using SSH** (Command shown above).

## Setting Up The Project

1. **Configure JavaFX in Your IDE:**
   - Add the JavaFX libraries under **Project Properties > Java Build Path** (if using Eclipse).

2. **Set Up the Database:**
   - Ensure your database system is running.
   - Update the database connection details in `DatabaseHelper.java` or related configuration files.

3. **Compile and Run the Application:**
   - In Eclipse, select **Project > Build Automatically**.
   - Run the application by opening `StartCSE360.java` and clicking **Run**.

## Testing the Application

1. **Set Up an Admin Account:**
   - Follow on-screen instructions to create an admin account.
   - Verify that the admin user is successfully created in the database.

2. **Test User Registration and Login:**
   - Create a new user account using the invitation code.
   - Attempt login with valid and invalid credentials to verify functionality.

3. **Discussion Page Testing:**
   - Add questions and verify their appearance in the UI.
   - Test adding answers to questions, editing, and deleting them.

4. **JUnit Tests Execution:**
   - Run your JUnit test cases under the `HW3` package to ensure full functionality.

5. **Check for Database Consistency:**
   - Ensure all CRUD operations are accurately reflected in the database.

## Generating Javadoc Documentation

To generate Javadoc documentation for your project, run the following command from the root directory:

```bash
javadoc -d doc -sourcepath src -subpackages HW3
```

This will generate HTML documentation files in the `doc` directory, which you can open with your browser.

---

## Additional Information

- The codebase is designed to be modular and extensible, making it easier to add new features in the future.
- All critical functionalities are covered by unit tests to ensure robustness and reliability.
- The user interface is designed to be simple yet effective, focusing on user interaction and usability.

If you encounter any issues or have suggestions for improvement, feel free to contribute by creating pull requests or raising issues in the repository.

Happy coding! 😊
