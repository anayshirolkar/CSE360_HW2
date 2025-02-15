```markdown
# Discussion Forum System

## Accessing the SSH Key

Before you can clone the repository, you'll need to set up an SSH key for authentication. Follow these steps to generate and add your SSH key to GitHub:

### 1. **Generate an SSH Key (if you don’t have one)**

If you haven't already generated an SSH key, you can do so by following these steps:

#### For Linux/macOS/Windows (Git Bash):
Open your terminal (or Git Bash) and run the following command to generate an SSH key:

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

This project is a **Discussion Forum system** designed to allow users to post questions, provide answers, and search through discussions effectively. The project has undergone several significant improvements, including the implementation of a UML-based class structure. This new design introduces proper object-oriented relationships between questions and answers, enhancing the system’s organization. Additionally, input validation and error handling have been incorporated to prevent invalid data entries, ensuring a smooth user experience. The search functionality has also been upgraded to make it easier for users to find relevant discussions.

Another major update includes the integration of **CRUD (Create, Read, Update, Delete) operations** with a database, allowing for the persistent storage and management of discussion threads. The code has been optimized by removing redundancies and improving overall efficiency. Comprehensive **unit tests** have been added to validate the system's key features, ensuring that it performs as expected. Detailed documentation and comments throughout the code improve readability and maintainability, making it easier for future developers to work with the project. Overall, these improvements make the **Discussion Forum system** more robust, user-friendly, and scalable.

## Prerequisites

Before you begin running the project, ensure that you have the following prerequisites installed:

- **Java Development Kit (JDK)** version 11 or later
- **JavaFX SDK**
- An **Integrated Development Environment (IDE)** such as **IntelliJ IDEA** or **Eclipse**

These tools will provide the necessary environment to compile and run the project successfully.

## Cloning the Repository

To access the project, you will need to clone the repository using **SSH**. Since the repository is private and SSH-protected, follow the instructions provided above to add your SSH key to GitHub and clone the repository.

### Steps:

1. **Generate an SSH Key** (if you haven't already)
2. **Add the SSH Key to GitHub**
3. **Clone the Repository Using SSH**

After downloading the project, you’ll need to configure a few components. JavaFX is required, and in Eclipse, you can add the JavaFX libraries under Project Properties > Java Build Path. Additionally, ensure that the database is running, and update the database connection details in the relevant configuration files, such as DatabaseHelper.java.

Once the setup is complete, you can proceed to run the project. In Eclipse, compile the project by selecting Project > Build Automatically, and then run the application by navigating to StartCSE360.java and clicking Run. This will launch the main application where you can begin testing the different features.

For testing, begin by setting up an admin account through the on-screen instructions. Verify that the admin user is successfully created in the database. Then, test the user registration and login functionality by creating a new user account with the invitation code and logging in with both correct and incorrect credentials. You should also test the Discussion Page by adding questions and ensuring they appear in the UI. Finally, test the ability to add answers to questions and edit or delete both questions and answers to verify the full functionality.
```

