# Admins - How To

This guide covers the shared setup steps plus the admin review step for approving pull requests and merging to main.

# 1. Prerequisites

1. Have Git installed
   - Install Git from [this link](https://git-scm.com/install/)
   - Click through the install, **YOU DO NOT NEED TO CHANGE ANY OPTIONS**
   - Once installed, close any open terminals if you have any open
   - Reopen the terminal (CMD, Powershell, Git Bash, etc.) and run the following command

     ```
     git --version
     ```

     If this returns a version number, Congrats! You have successfully installed Git
     At the time of writing, the current windows git version is "2.54.0.windows.1"

     If there are errors, try running the installer again

- Run the following commands to configure Git with your Github information

  ```
  git config --global user.name "{Put Your Full Name Here}"
  ```

  //example: git config --global user.name "John Doe"

  ```
  git config --global user.email "{Put Your Email Here}"
  ```

  //example: git config --global user.email "johndoe@gmail.com"

2. Have VSCode installed (That is what this guide uses, feel free to use other editors)
   - Install VSCode from [this link](https://code.visualstudio.com/download)
   - Click through the install, **YOU DO NOT NEED TO CHANGE ANY OPTIONS**
   - Launch VSCode and sign into your Github account
   - Install the GitHub Pull Requests extension.
     - Go to the Extensions tab in the sidebar and search for "GitHub Pull Requests" </br>  
     <img title="" src="../README-assets/2026-05-14-103813.png" alt="" data-align="center">
     - Install the extension
   - Install the Live Preview extension.
     - Go to the Extensions tab in the sidebar and search for "Live Preview" </br>  
     <img title="" src="../README-assets/2026-05-15-112642.png" alt="" data-align="center">
     - Install the extension

# 2. Cloning The Repository

### NOTE: If you have already done this, SKIP TO THE NEXT STEP.<!-- omit from toc -->

1. Go to where you want to clone the repository, right click within the directory and select **"Open in Terminal"**

   //example: project folder in the Documents Folder

<img title="" src="../README-assets/1c65d76cc7436d1cf1fc2aded2c496694b01e29a.png" alt="" data-align="center">

2. Within the terminal, type in

```
git clone --branch templates https://github.com/Tims-Sims/simulations.git
```

3. After cloning, move into the simulations directory

```
cd simulations
```

4. Open in VSCode

```
code .
```

# 3. Switching to Another Branch

You can switch branches both within the terminal and on VSCode. We will go through how to do so on both.

## 3.1. VSCode

1. Go to the "Source Control" tab in the sidebar
   
   <img title="" src="../README-assets/2026-05-14-112308.png" alt="" data-align="center">
2. Click the three dots (...) within the "CHANGES" bar
   
   <img title="" src="../README-assets/2026-05-14-112612.png" alt="" data-align="center">
3. Click "Fetch"
   
   <img title="" src="../README-assets/2026-05-14-11272.png" alt="" data-align="center">

4. Click the button to the left of the "Synchronize" button that shows the name of the current branch you are on, search for the branch name and select it to switch branches

<img title="" src="../README-assets/1b26bba13fa415467f24c9a7fceb9f009202872c.png" alt="" data-align="center">

### NOTE: When you start a development session, you should always fetch <!-- omit from toc -->

## 3.2. Terminal

1. The fetch command updates the available branches

```
git fetch
```

2. Now switch branches by using git switch

```
git switch {branch-name}
```

//example: git switch ELAF1T2U4S5

# 4. Pulling Changes

Changes made and pushed by others do not automatically show up, you must pull updates from the repository. This can be for many reasons such as a tester that is currently testing a branch while the developer is making changes

You can pull changes both within the terminal and on VSCode. We will go through how to do so on both

## 4.1. VSCode

1. Use the "Synchronize" button in VSCode

<img title="" src="../README-assets/b3b0ca493e35426e6b7890e6ef0fb25cc6e91e7d.png" alt="" data-align="center">

## 4.2. Terminal

1. Pull Changes using the following command

   ```
   git pull
   ```

### NOTE: You should periodically pull, especially if you just switched to the branch <!-- omit from toc -->

# 5. Pull Request Review & Approval

1. The content liaison for the created sim subject and an admin tester would review the Pull Request one final time to ensure quality.

2. Each reviewer would submit a review where they can approve or note changes to be made.

3. If changes need to be made, once the developer makes them, it would show up on the Pull Request thread, allowing the reviewer to once again submit a review.

4. Once all reviewers have approved the Pull Request, an admin can finally merge the sim into the main branch.
