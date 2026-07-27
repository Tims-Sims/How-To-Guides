# How to Use <!-- omit from toc -->

This guide shows the overall process of simulation creation.

<!--
The [Appendix](#13-appendix) holds quick explanation of terms used among others
-->

Steps related to your role are shown and linked in the table below

# Team-relevant Sections <!-- omit from toc -->

| Role             | Relevant Topics |
| ---------------- | :-------------- |
| All | [Prerequisites](#1-prerequisites) \| [Cloning The Repository](#2-cloning-the-repository) \| [Switching to Another Branch](#5-switching-to-another-branch) \| [Pulling Changes](#7-pulling-changes) |
| Content Liaisons | [Creating a New Branch and Issue](#3-creating-a-new-branch-and-issue) \| [Leaving Comments](#9-leaving-comments) \| [Pull Request Review \& Approval](#11-pull-request-review--approval) |
| Developers       | [Assigning Yourself to an Issue](#4-assigning-yourself-to-an-issue) \| [File Structure](#6-file-structure) \| [Committing Changes](#8-committing-changes) |
| QA Testers       | [Leaving Comments](#9-leaving-comments) \| [Pull Requests](#10-pull-requests) \| [Pull Request Review \& Approval](#11-pull-request-review--approval) |
| Admins           | [Pull Request Review \& Approval](#11-pull-request-review--approval) |

# Table of Contents <!-- omit from toc -->

- [1. Prerequisites](#1-prerequisites)
- [2. Cloning The Repository](#2-cloning-the-repository)
- [3. Creating a New Branch and Issue](#3-creating-a-new-branch-and-issue)
- [4. Assigning Yourself to an Issue](#4-assigning-yourself-to-an-issue)
- [5. Switching to Another Branch](#5-switching-to-another-branch)
  - [5.1. VSCode](#51-vscode)
  - [5.2. Terminal](#52-terminal)
- [6. File Structure](#6-file-structure)
- [7. Pulling Changes](#7-pulling-changes)
  - [7.1. VSCode](#71-vscode)
  - [7.2. Terminal](#72-terminal)
- [8. Committing Changes](#8-committing-changes)
  - [8.1. General Information](#81-general-information)
  - [8.2. VSCode](#82-vscode)
  - [8.3. Terminal](#83-terminal)
- [9. Leaving Comments](#9-leaving-comments)
- [10. Pull Requests](#10-pull-requests)
- [11. Pull Request Review \& Approval](#11-pull-request-review--approval)
- [12. Delete This README if you haven't already](#12-delete-this-readme-if-you-havent-already)
- [Workflow Flowcharts](#workflow-flowcharts)
  - [General Flow](#general-flow)
  - [Content Liason Flow](#content-liason-flow)
  - [Dev Flow](#dev-flow)
  - [Tester Flow](#tester-flow)


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
     <img title="" src="./README-assets/2026-05-14-103813.png" alt="" data-align="center">
     - Install the extension
   - Install the Live Preview extension.
     - Go to the Extensions tab in the sidebar and search for "Live Preview" </br>  
     <img title="" src="./README-assets/2026-05-15-112642.png" alt="" data-align="center">
     - Install the extension


# 2. Cloning The Repository

### NOTE: If you have already done this, SKIP TO THE NEXT STEP.<!-- omit from toc -->

1. Go to where you want to clone the repository, right click within the directory and select **"Open in Terminal"**

   //example: project folder in the Documents Folder

<img title="" src="./README-assets/1c65d76cc7436d1cf1fc2aded2c496694b01e29a.png" alt="" data-align="center">

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

# 3. Creating a New Branch and Issue

1. In the [simulations repository](https://github.com/Tims-Sims/simulations), click on **main** and in the drop down, select "View all branches" **OR** Go to [this link](https://github.com/Tims-Sims/simulations/branches)

   <img title="" src="./README-assets/c183b0d1240c605006d8d239ef8792cc7e4ddc3e.png" alt="" data-align="center">

2. Click **"New Branch"**

3. Select the source as **templates**

4. Name the branch after the name of the simulation to be made, following the naming convention

   > ## Naming Convention
   >
   > ### Main Subjects
   > | Subject | Abbreviation |
   > |---------|--------------|
   > | English Language Arts| ELA |
   > | Mathematics| MATH |
   > | Integrated Science| SCI |
   > | Information Technology| IT |
   > | Social Sciences| SS |
   > | Spanish| SPAN |
   >
   > ### Integrated Science Subjects
   > | Subject | Abbreviation |
   > |---------|--------------|
   > | Fundamentals| FUND |
   > | Physics| PHYS |
   > | Chemistry| CHEM |
   > | Biology| BIO |
   >
   > ### Social Science Subjects
   > | Subject | Abbreviation |
   > |---------|--------------|
   > | Social Studies| SOC |
   > | Geography| GEO |
   > | History| HIST |
   >
   > {Subject}{Form}{Term}{Unit}{Section}{Sim}
   >
   > //example: English, Form 1, Term 2, Unit 4, Section 5, Sim 1=== ELA-F1-T2-U4-SEC5-SIM1
   >
   > ---
   > For subjects like Integrated Science and Social Science with sub-subjects there is an additional folder
   >
   > {Main Subject}{Subject}{Form}{Term}{Unit}{Section}{Sim}
   >
   > //example: Social Science, History, Form 1, Term 2, Unit 4, Section 5, Sim 1 === </br>
   >SS-HIST-F1-T2-U4-SEC5-SIM1

5. Open an issue (Top Bar -> Issues -> New Issue) and name it the same as the branch created

   <img title="" src="./README-assets/fe50699b483e33c2cb8de4e7b20c8f010789a3d3.png" alt="" data-align="center">

6. In the description, put the Simulation spec provided by the content team
7. Set the issue label to **"dev needed"**

   <img title="" src="./README-assets/ab44614cd96de633902c4c9d7db7bf71e44e98b6.png" alt="" data-align="center">

   Once created, set the Development branch as the branch created

   <img title="" src="./README-assets/33674f7e99f0d42a53fec81484cfd304522b9a12.png" alt="" data-align="center">

# 4. Assigning Yourself to an Issue

1. In the Issues tab in the top bar, click the labels button and in the drop down, select the "dev needed" label to filter only issues that need developers
    
   <img title="" src="./README-assets/2026-05-14-141638.png" alt="" data-align="center">

2. Once you have selected an issue that needs a developer, click the "assign yourself" button to assign yourself to the issue
   
   <img title="" src="./README-assets/2026-05-14-142505.png" alt="" data-align="center">
   
3. Remove the "dev needed" label and select the "in progress" label
   
   <img title="" src="./README-assets/2026-05-14-142738.png" alt="" data-align="center">

4. Now that you have assigned yourself, you can see the Issue thread within the Github Pull Requests extension inside of VSCode
5. Click the Github logo button in the sidebar
   
   <img title="" src="./README-assets/2026-05-15-094917.png" alt="" data-align="center">

6. In the Issues Section, you can see all issues you are assigned to and can do various things such as seeing the issue name, changing labels and assigning others without leaving VSCode. 
   
   <img title="" src="./README-assets/2026-05-15-095654.png" alt="" data-align="center">

# 5. Switching to Another Branch

You can switch branches both within the terminal and on VSCode. We will go through how to do so on both.

## 5.1. VSCode

1. Go to the "Source Control" tab in the sidebar
   
   <img title="" src="./README-assets/2026-05-14-112308.png" alt="" data-align="center">
2. Click the three dots (...) within the "CHANGES" bar
   
   <img title="" src="./README-assets/2026-05-14-112612.png" alt="" data-align="center">
3. Click "Fetch"
   
   <img title="" src="./README-assets/2026-05-14-11272.png" alt="" data-align="center">

4. Click the button to the left of the "Synchronize" button that shows the name of the current branch you are on, search for the branch name and select it to switch branches

<img title="" src="./README-assets/1b26bba13fa415467f24c9a7fceb9f009202872c.png" alt="" data-align="center">

### NOTE: When you start a development session, you should always fetch <!-- omit from toc -->

## 5.2. Terminal

1. The fetch command updates the available branches

```
git fetch
```

2. Now switch branches by using git switch

```
git switch {branch-name}
```

//example: git switch ELA-F1-T2-U4-SEC5-SIM1

# 6. File Structure

**ENSURE FILE STRUCTURE IS PRESENT SO THAT THERE WILL BE NO MERGE CONFLICTS**

1. Select the template file you want to use and rename it
2. Delete the other template files
3. Create the file structure **BEFORE** beginning to work  
   > ### File Structure
   >
   > {Subject} -> {Form} -> {Term} -> {Unit} -> [Your HTML File Here]
   > As you can see, the naming convention follows the file structure
   >
   > //example: ELA-F1-T2-U4-SEC5-SIM1 === ELA => Form1 => Term2 => Unit4 => Section5 => Simulation1 => ELA-F1-T2-U4-SEC5-SIM1
   >
   > ![](./README-assets/2026-05-13-105644.png)
   >
   > //example: SS-HIST-F1-T2-U4-SEC5-SIM1 === SS => HIST => Form1 => Term2 => Unit4 => Section5 => Simulation1 => SS-HIST-F1-T2-U4-SEC5-SIM1
   >
   > ![](./README-assets/2026-05-13-105858.png)
   
### NOTE: You should only have ONE HTML file that you are working on <!-- omit from toc -->


# 7. Pulling Changes

Changes made and pushed by others do not automatically show up, you must pull updates from the repository. This can be for many reasons such as a tester that is currently testing a branch while the developer is making changes

You can pull changes both within the terminal and on VSCode. We will go through how to do so on both

## 7.1. VSCode

1. Use the "Synchronize" button in VSCode

<img title="" src="./README-assets/b3b0ca493e35426e6b7890e6ef0fb25cc6e91e7d.png" alt="" data-align="center">

## 7.2. Terminal

1. Pull Changes using the following command

   ```
   git pull
   ```

### NOTE: You should periodically pull, especially if you just switched to the branch <!-- omit from toc -->

# 8. Committing Changes

You can commit changes both within the terminal and on VSCode. We will go through how to do so on both.

## 8.1. General Information

1. When committing changes, ALWAYS start the commit messages with the issue number, this makes the commit show up within the issue thread.
   //example: #9999 fixed x, y and z

2. Go to the issue and set the label to **review needed**

3. Repeat steps as needed
   
4. While developing, you can see the simulation using the Live Preview extension, right-click the sim file and select the "Show Preview" button
   
   <img title="" src="./README-assets/2026-05-15-121859.png" alt="" data-align="center">

## 8.2. VSCode

1. Once you have made changes, go to source control in VSCode to see all the files you have changed

<img title="" src="./README-assets/439a6c837fa2884b20cfc8c7d3a06eef9d49fdba.png" alt="" data-align="center">

2. Stage your changes by clicking the **"+"** buttons, use the **"+"** next to "Changes" to stage all changes

   <img title="" src="./README-assets/a3f54dc4103cd37d9a3d7c78937494c7f55d7c89.png" alt="" data-align="center">

3. Type your commit message in the text box and click commit

   <img title="" src="./README-assets/43743cfe4b7947fc7143750ad2e68f2611a0abb0.png" alt="" data-align="center">

4. Once you have made a commit, you must push your changes by clicking
   "Sync Changes"

   <img title="" src="./README-assets/80eac4c99bd1e535bb772a94e5d0d4d2f1619083.png" alt="" data-align="center">

## 8.3. Terminal

1. Once you are within the code directory, stage your changes

```
git add {file1} {file2}
```

If you do not know what files can be staged, check with

```
git status
```

### OR <!-- omit from toc -->

stage everything using the command

```
git add .
```

2. Once you have staged, commit your changes

```
git commit -m "#{issue number} {comment}"
```

3. Finally, push your changes

```
git push
```

### NOTE <!-- omit from toc -->

If it is your first push on the branch, you should set the upstream with your first push using

```
git push -u origin {branch-name}
```

# 9. Leaving Comments

1. In the Issues tab in the top bar, click the labels button and in the drop down, select the **"review needed"** label to filter only issues that are ready to be reviewed
   
   <img title="" src="./README-assets/2026-05-14-143358.png" alt="" data-align="center">

2. Once you have selected an issue that needs reviewing, click the Assignees button to assign yourself to the issue. You may have to search for your name
   
   <img title="" src="./README-assets/2026-05-14-144339.png" alt="" data-align="center">

3. You can click on the commit made to see the differences in the code

   <img title="" src="./README-assets/be03ae3223ddb45120eb7daecd66a5e2bf740370.png" alt="" data-align="center">

4. Copy the commit hash (the number next the the word Commit in the title) and view the changes in red and green (the Git Diff). Testers can also pull the changes and test that way ([See Pulling Changes](#7-pulling-changes)).

   <img title="" src="./README-assets/4b83c98699ce9167a49126e2683c61b9263214d4.png" alt="" data-align="center">

5. You can test the simulation using the VSCode Live Preview extension, right-click the sim file and select the "Show Preview" button
   
   <img title="" src="./README-assets/2026-05-15-121859.png" alt="" data-align="center">

6. Leave a comment starting with the commit hash so that it links to the specific commit and change the label to **changes needed**

   <img title="" src="./README-assets/ed3f5a637f056f1d1c9b702f508f10a32dc56b38.png" alt="" data-align="center">

# 10. Pull Requests

1. Once a sim is labelled **done** in its specific issue thread, testers may open a pull request to merge into main

2. Go to **Pull Requests** and click **"Create Pull Request"**

   <img title="" src="./README-assets/3825c9370df08b3f6d110cb4a8f587c45f6c5767.png" alt="" data-align="center">

3. Set base as **main**

4. Set compare as the branch you want to merge

   <img title="" src="./README-assets/0628cd38c03f1aac1b565cb431ab0cc5ebb8aa2f.png" alt="" data-align="center">

5. Create Pull Request and rename to ensure it is the same as the branch (PR names generate a bit weird so you 99% will have to change it)

# 11. Pull Request Review & Approval

1. The content liaison for the created sim subject and an admin tester would review the Pull Request one final time to ensure quality.

2. Each reviewer would submit a review where they can approve or note changes to be made.

3. If changes need to be made, once the developer makes them, it would show up on the Pull Request thread, allowing the reviewer to once again submit a review.

4. Once all reviewers have approved the Pull Request, an admin can finally merge the sim into the main branch.

# 12. Delete This README if you haven't already

# Workflow Flowcharts
## General Flow
<img title="" src="./README-assets/Sims-General-Flow-Chart.png" alt="" data-align="center">

## Content Liason Flow
<img title="" src="./README-assets/Content-Liaison-WorkFlow.png" alt="" data-align="center">

## Dev Flow
<img title="" src="./README-assets/DEV-Dev-WorkFlow.png" alt="" data-align="center">

## Tester Flow
<img title="" src="./README-assets/Tester-WorkFlow.png" alt="" data-align="center">

<!--
# 13. Appendix
## 13.1. Git Commands
| Command | What It Does |
| ------- | ------------ |
|||

## 13.2. Github Terms
| Term | What It Does |
| ---- | ------------ |
|||

## 13.3. VSCode Terms
| Term | What It Does |
| ---- | ------------ |
|||
-->
