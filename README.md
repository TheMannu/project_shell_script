# shell_script_project :- This Bash script is designed to list users who have read access to a specific GitHub repository. Below is a use case scenario and the steps to run the script:

## Use Case:
Suppose you are managing a GitHub repository, and you need to know which users have been granted read access to it. This information might be crucial for monitoring repository access or managing collaboration permissions.

## Steps to Run the Script:
1. **Set Up GitHub Personal Access Token:**
   - foe running the script,we need to generate a `personal access token` from GitHub.We can create GItHub account settings, selecting "Developer settings," --> "Personal access tokens," and generat a new token with required permissions (at least `repo` scope is required for the script).
   
2. **Set Up Script Variables:**
   - Open the script folder (`github-api`) in a text editor.
   - Run the command  (`chmod 770 listing-user-in-project.sh`).
   - Also the script need  jq  in the env , so Run this command to setup jq(`sudo apt install jq - y`) 
   - Expor the values for `USERNAME` and `TOKEN` variables to your GitHub username and the personal access token you generated 
   - Run the command (`export username="YourGitHubUsername"`)for exporting uername.
   - Run the command (`export token="YourGitHubPAT"`) for exporting the token.
 
3. **Provide Repository Information:**
   - Decide which repository you want to check for read access.
   - Call the script from the command line with the repository owner's username and the repository name as arguments. For example:
 
     bash listing-user-in-project.sh repo_owner repo_name
 
     Replace `repo_owner` and `repo_name` with the actual GitHub username and repository name, respectively.

4. **Execute the Script:**
   - Open a terminal or command prompt.
   - Navigate to the directory where the script file is located.
   - Run the script by typing:
 
     bash listing-user-in-project.sh repo_owner repo_name
 
     Replace `repo_owner` and `repo_name` with the actual GitHub username and repository name, respectively.
 
5. **Review Output:**
   - The script will make a request to the GitHub API and display a list of users who have read access to the specified repository.
   - If no users with read access are found, it will display a corresponding message.

6. **Review Access Permissions:**
   - Once the script finishes executing, review the list of users with read access to ensure it aligns with your expectations.
   - You can adjust repository permissions as needed through the GitHub interface.

By following these steps, you can easily identify users with read access to a GitHub repository using the provided Bash script.
