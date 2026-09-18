WEDNESDAY 16: SETTING UP GITHUB IN UBUNTU TERMINAL

Phase 1: Local Setup & File Creation
First, you create the workspace on your Ubuntu machine and create your project files.

   1. Create and enter a new project directory:
   mkdir devops15 && cd devops15

   2. Initialize Git in the folder:
   git init

   3. Add a file to the directory:
   echo "# DevOps 15 Project" > README.md

------------------------------
Phase 2: Generating SSH Keys (One-Time Setup)
Before interacting with GitHub via SSH, your computer needs an identity key registered on your GitHub account.

   1. Generate the SSH Key:
   ssh-keygen -t ed25519 -C "your_email@example.com"
   (Press Enter to accept all default prompts).

   2. Copy the public key:
   cat ~/.ssh/id_ed25519.pub
   (Copy the entire line starting with ssh-ed25519).

   3. Add to GitHub:
   Go to GitHub -> Settings -> SSH and GPG keys -> New SSH key, and paste your key.

------------------------------
Phase 3: Getting the URL, Linking, and Staging
Now that SSH is ready, you connect your local Git environment to the cloud.

   1. Get the Remote SSH URL from GitHub:
      - Go to your repository page on GitHub.
      - Click the green Code button.
      - Select the SSH tab (not HTTPS).
      - Copy the URL, e.g.: git@github.com:nabiswavalencia/devops15.git

   2. Link the remote repository to your folder:
   git remote add origin git@github.com:nabiswavalencia/devops15.git

   3. Check and stage your changes:
   git status
   git add .

   4. Commit the changes locally:
   git commit -m "Initial commit"

------------------------------
Phase 4: Checking Branches & Pushing
Before sending code to GitHub, ensure your branches align with modern Git standards.

   1. Check your current active branch:
   git branch

   2. Rename the default branch to main (if your terminal defaulted to master):
   git branch -M main

   3. Push to the remote repository:
   git push -u origin main
   (Type yes if prompted with a security fingerprint message).

------------------------------
Phase 5: Cloning the SSH Repo Elsewhere
If you or a teammate ever need to download this complete project onto a different folder or a new machine using SSH:

   1. Clone the repository:
   git clone git@github.com:nabiswavalencia/devops15.git
