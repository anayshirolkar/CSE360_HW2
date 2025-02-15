# CSE360_HW2
# Discussion Forum System

## Accessing the SSH Key

Before you can clone the repository, you'll need to set up an SSH key for authentication. Follow these steps to generate and add your SSH key to GitHub:

### 1. **Generate an SSH Key (if you don’t have one)**

If you haven't already generated an SSH key, you can do so by following these steps:

#### For Linux/macOS/Windows (Git Bash):
Open your terminal (or Git Bash) and run the following command to generate an SSH key:

```bash
ssh-keygen -t ed25519 -C "anayshirolkar@gmail.com"

ssh-keygen -t rsa -b 4096 -C "anayshirolkar@gmail.com"

SSH Key
cat ~/.ssh/id_ed25519.pub

If you are using RSA
cat ~/.ssh/id_rsa.pub

Clone the Repo using this link
git clone git@github.com:anayshirolkar/CSE360_HW2.git


This project is a Discussion Forum system designed to allow users to post questions, provide answers, and search through discussions effectively. The project has undergone several significant improvements, including the implementation of a UML-based class structure. This new design introduces proper object-oriented relationships between questions and answers, enhancing the system’s organization. Additionally, input validation and error handling have been incorporated to prevent invalid data entries, ensuring a smooth user experience. The search functionality has also been upgraded to make it easier for users to find relevant discussions.


Another major update includes the integration of CRUD (Create, Read, Update, Delete) operations with a database, allowing for the persistent storage and management of discussion threads. The code has been optimized by removing redundancies and improving overall efficiency. Comprehensive unit tests have been added to validate the system's key features, ensuring that it performs as expected. Detailed documentation and comments throughout the code improve readability and maintainability, making it easier for future developers to work with the project. Overall, these improvements make the Discussion Forum system more robust, user-friendly, and scalable.


Before you begin running the project, ensure that you have the following prerequisites installed: the Java Development Kit (JDK) version 11 or later, the JavaFX SDK, and an Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse. These tools will provide the necessary environment to compile and run the project successfully.


To access the project, you will need to clone the repository using SSH. Since the repository is private and SSH-protected, follow the instructions provided to add your SSH key to GitHub and clone the repository. First, generate an SSH key if you haven't already, then add the public key to your GitHub account under Settings > SSH and GPG Keys. Once your key is added, you can securely clone the repository using SSH and navigate into the project directory.


After downloading the project, you’ll need to configure a few components. JavaFX is required, and in Eclipse, you can add the JavaFX libraries under Project Properties > Java Build Path. Additionally, ensure that the database is running, and update the database connection details in the relevant configuration files, such as DatabaseHelper.java.

Once the setup is complete, you can proceed to run the project. In Eclipse, compile the project by selecting Project > Build Automatically, and then run the application by navigating to StartCSE360.java and clicking Run. This will launch the main application where you can begin testing the different features.

For testing, begin by setting up an admin account through the on-screen instructions. Verify that the admin user is successfully created in the database. Then, test the user registration and login functionality by creating a new user account with the invitation code and logging in with both correct and incorrect credentials. You should also test the Discussion Page by adding questions and ensuring they appear in the UI. Finally, test the ability to add answers to questions and edit or delete both questions and answers to verify the full functionality.
