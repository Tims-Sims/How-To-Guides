# Content Liaisons - How To

This guide covers the shared setup steps plus the content liaison workflow for opening branches, managing reviews, and approving pull requests.

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

# 5. Creating a New Branch and Issue

1. In the [simulations repository](https://github.com/Tims-Sims/simulations), click on **main** and in the drop down, select "View all branches" **OR** Go to [this link](https://github.com/Tims-Sims/simulations/branches)

   <img title="" src="../README-assets/c183b0d1240c605006d8d239ef8792cc7e4ddc3e.png" alt="" data-align="center">

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

   > ## Maths (MATH)
   >
   > Maths branches are named DIFFERENTLY. Maths does not use the F1-T2-U4 style. It uses the curriculum code — 4 numbers with dots, like `1.5.4.2`:
   > 1. First number = the Form (the class year).
   > 2. Second number = the Strand (the big maths area, like Measurement).
   > 3. Third number = the Topic (like Area).
   > 4. Fourth number = the Learning Outcome (the exact thing students learn).
   >
   > So a maths branch name looks like this: `MATH-1.1.1.1-SIM1`
   > 1. Start with `MATH-`.
   > 2. Then the 4-number code.
   > 3. Then `-SIM` and a number. Always add `-SIM1` even if it is the only sim.
   > 4. Never write `01` — just write `1`.
   >
   > You do NOT make up the code. It is written in the sim spec (in the GitHub issue). If it is not there, ask for it.
   >
   > The issue name and the pull request title must be exactly the same as the branch name.

5. Open an issue (Top Bar -> Issues -> New Issue) and name it the same as the branch created

   <img title="" src="../README-assets/fe50699b483e33c2cb8de4e7b20c8f010789a3d3.png" alt="" data-align="center">

6. In the description, put the Simulation spec provided by the content team
7. Set the issue label to **"dev needed"**

   <img title="" src="../README-assets/ab44614cd96de633902c4c9d7db7bf71e44e98b6.png" alt="" data-align="center">

   Once created, set the Development branch as the branch created

   <img title="" src="../README-assets/33674f7e99f0d42a53fec81484cfd304522b9a12.png" alt="" data-align="center">

# 6. Leaving Comments

1. In the Issues tab in the top bar, click the labels button and in the drop down, select the **"review needed"** label to filter only issues that are ready to be reviewed
   
   <img title="" src="../README-assets/2026-05-14-143358.png" alt="" data-align="center">

2. Once you have selected an issue that needs reviewing, click the Assignees button to assign yourself to the issue. You may have to search for your name
   
   <img title="" src="../README-assets/2026-05-14-144339.png" alt="" data-align="center">

3. You can click on the commit made to see the differences in the code

   <img title="" src="../README-assets/be03ae3223ddb45120eb7daecd66a5e2bf740370.png" alt="" data-align="center">

4. Copy the commit hash (the number next the the word Commit in the title) and view the changes in red and green (the Git Diff). Testers can also pull the changes and test that way.

   <img title="" src="../README-assets/4b83c98699ce9167a49126e2683c61b9263214d4.png" alt="" data-align="center">

5. You can test the simulation using the VSCode Live Preview extension, right-click the sim file and select the "Show Preview" button
   
   <img title="" src="../README-assets/2026-05-15-121859.png" alt="" data-align="center">

6. Leave a comment starting with the commit hash so that it links to the specific commit and change the label to **changes needed**

   <img title="" src="../README-assets/ed3f5a637f056f1d1c9b702f508f10a32dc56b38.png" alt="" data-align="center">

# 7. Pull Request Review & Approval

1. The content liaison for the created sim subject and an admin tester would review the Pull Request one final time to ensure quality.

2. Each reviewer would submit a review where they can approve or note changes to be made.

3. If changes need to be made, once the developer makes them, it would show up on the Pull Request thread, allowing the reviewer to once again submit a review.

4. Once all reviewers have approved the Pull Request, an admin can finally merge the sim into the main branch.
