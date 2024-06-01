# autoGIT-cli

autoGIT-cli is a command-line interface (CLI) tool designed to simplify the process of uploading files to GitHub repositories. It consists of several Python scripts that interact with the GitHub API and manage local file operations.

## Key Components

1. **git_uploader.py:**
   - Contains the `GitHubUploader` class for handling GitHub API interactions.
   - Responsible for authentication, listing repositories, selecting repositories, and uploading files to GitHub.

2. **files.py:**
   - Includes the `FileManager` class for managing local file operations.
   - Provides functionalities to list files in the current directory, select files for upload, and get file paths.

3. **autoGIT.py:**
   - Main script that integrates `git_uploader.py` and `files.py` to facilitate file uploads to GitHub repositories.
   - Utilizes user input to select files, enter commit messages, and upload files to the chosen repository.

4. **run.sh:**
   - A bash script for setting up the `autoGIT` command alias and creating `secrets.ini` for GitHub API credentials.
   - Automates the process of configuring the environment and gathering necessary information for GitHub API access.

## Usage
1. Clone the Repository :
```bash
git clone https://github.com/ky13-troj/autoGIT-cli.git
```
2. Navigate to the cloned directory :
```bash
cd autoGIT-cli
```
3. Give execution Permission to run.sh :
```bash
chmod +x run.sh
```
4. Run the run.sh script to set up the autoGIT command and provide GitHub API credentials :
```bash
bash run.sh
```
___

Follow the prompts to enter your GitHub API secret key and username. This will create the necessary configuration files and setup the autoGIT command alias.

4. Now you can use the autoGIT command from anywhere to upload files to your selected GitHub repository :
```bash
autoGIT
```
___
Follow the interactive prompts to select files, enter commit messages, and upload files to GitHub.

## Steps to get the Github API access key :
1. Sign in to GitHub:

- Open your web browser and go to GitHub.
- Sign in to your GitHub account if you are not already signed in.
  
2. Navigate to Developer Settings:

- Click on your profile icon at the top right corner of the GitHub page.
- From the dropdown menu, select "Settings."

3. Access Personal Access Tokens:

- In the settings sidebar, scroll down and click on "Developer settings."
- From the developer settings sidebar, click on "Personal access tokens."

4. Generate New Token:

- On the "Personal access tokens" page, click on the "Generate new token" button.
5. Provide Token Information:

- Enter a descriptive note for your token in the "Note" field to remember its purpose.
- Select the scopes (permissions) you want to grant to this token. Make sure to only select the scopes necessary for your use case to minimize security risks. (You can select all of them too ;) 

6. Generate Token:

- After selecting scopes and providing a note, click on the "Generate token" button.

7. Copy and Save Token:

- Once the token is generated, you will see it displayed on the screen.
- Copy the generated token immediately and save it securely. GitHub will not show this token again.

8. Use Token Safely:

- Treat your GitHub API token like a password and keep it secure.
- Do not share your token publicly or embed it directly in your code repositories.
- Use environment variables or secure configuration files (like secrets.ini) to manage and access your API token securely in your code.

9. Revoke Token if Needed:

- If you suspect that your token has been compromised or you no longer need it, you can revoke the token from the "Personal access tokens" page in your GitHub settings.
___
Current Issues :
1. Doesn't support new repository creation
2. Unable to upload secrets files

____

## Structure
autoGIT-cli/
│
├── README.md
├── run.sh
├── git_uploader.py
├── files.py
├── autoGIT.py
├── secrets.ini
├── LICENSE

___

# Contribution
We welcome contributions to the autoGIT-cli project! Here are a few ways you can contribute:

1. Report Issues: If you encounter any bugs or have suggestions for improvements, please open an issue on GitHub.
2. Submit Pull Requests: Feel free to fork the repository, make changes, and submit pull requests for new features or bug fixes.
3. Documentation: Help improve the project's documentation by fixing typos, adding examples, or clarifying instructions.
4. Spread the Word: Share the project with others, star the repository on GitHub, and let others know about your experience using autoGIT-cli.

___
medium Blog link : [click here](https://ky13-troj.medium.com/simplifying-github-operations-with-autogit-cli-44534d3c2b500

Happy Coding :3
