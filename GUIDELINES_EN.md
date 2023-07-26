# DUO Style Guide

## Table of Contents

1. [**PROJECT'S LINKS**](#1-projec-s-links)\
   1.1 [Project's Links](#11-project-links) 

2. [**WORK PROCEDURES**](#2-work-procedures)\
   2.1 [First things to do in the project](#21-first-things-to-do-in-the-project)\
   2.2 [Git configurations](#22-git-configurations)\

3. [**CODING GUIDELINES**](#3-definitions-of-method,-class,-etc...)
   
4. [**STACK**](#4-stack)\
   4.1 [Framework](#41-framework)\
   4.2 [Libraries](#42-libraries)

5. [**REQUISITES**](#5-requisites)

6. [**INSTALLATION**](#6-installation)

7. [**DEVELOPMENT**](#6-installation)

8. [**TESTING**](#6-installation)

----------------------------------------------------------------

# 1. PROJECT'S LINKS
## 1.1 Project links
- [GITHUB](https://github.com/HectorRamirezGarcia/DUO)
- [Frontend Sprint Backlog](https://github.com/users/HectorRamirezGarcia/projects/1/views/2)
- [Figma](https://www.figma.com/file/me6M8lyBDUSHaDTmqiu7RQ/Duo?type=design&t=ml9x3NbWUlGQYmgp-6)

----------------------------------------------------------------

# 2. WORK PROCEDURES

## 2.1 First things to do in the project
### 0. Ask permission to collaborate with the project

### 1. Add your name to the file contributors.md

1. Clone the Github repository ita-challenges-frontend in your local system:

         git clone https://github.com/HectorRamirezGarcia/DUO.git
2. Move to the directory of the cloned repository:

         cd duo-frontend
3. You can verify the available branches and your current branch by running the following command:

         git branch
4. If you are not on the "develop" branch, switch to it by executing the following command::

         git switch develop
5. Create a new branch with your name to make your changes:

         git switch -c your-branch-name
   Replace "your-branch-name" with a descriptive name that indicates the changes you plan to make.


6. Open the contributors.md file and add your name and GitHub username.


7. After doing a 'git add' and 'git commit', perform the following 'git push':

         git push origin your-branch-name
8. Open the repository on GitHub. You should see a message that allows you to create a pull request from your newly created branch to the "develop" branch. Click on the link to create the pull request.

----------------------------------------------------------------

## 2.2 Git configurations

Necessary Git configurations to prevent problems

### 2.2.1 Git ignore
1. Edit the .gitignore file:
If necessary, you can now edit the ".gitignore" file to include any specific file or directory patterns that you want Git to ignore across all your projects. Remember to save the file after making any changes.

2. Propagate changes:
Changes in your .gitignore file will not retroactively affect files that have already been tracked by Git. If you want Git to start ignoring a file that was previously tracked, you must first untrack this file. Use the command 'git rm --cached filename' to untrack a file. For the changes to take effect, you'll need to commit this change.

3. Avoid sensitive data:
A good practice is to include files containing sensitive data (like configuration files with passwords or API keys) in your .gitignore file. This will prevent such files from being accidentally committed to your repository.

4. Global vs local .gitignore:
Remember, the global ".gitignore" file will apply to all your Git projects. If you have files to be ignored that are specific to a single project, consider using a local ".gitignore" file within that project's directory.

### 2.2.2 Autocrlf
1. Open Git Bash.
2. Run the following command to configure the autocrlf setting globally:

        git config --global core.autocrlf true
The autocrlf setting handles line-ending differences between different operating systems. Enabling it ensures consistent line endings across different platforms when working with Git.

3. Provide context: Modifying a large number of files in a PR can introduce issues related to inconsistent line endings. This configuration helps maintain consistent line endings and prevents potential problems when collaborating across different platforms.

4. Examples and considerations: Here are a few scenarios where the autocrlf setting can be helpful:

- Collaboration: When multiple developers are working on a project, each using a different operating system, enabling autocrlf ensures that line endings are automatically adjusted to be consistent.

- Deployment: If your project requires specific line endings for deployment purposes (e.g., Unix-style line endings on a Linux server), enabling autocrlf ensures the line endings are automatically converted during checkout and commit.

- Caveats: Enabling autocrlf may have some trade-offs. It's important to be aware that automatic line-ending conversions can sometimes introduce unintended changes to files. It's recommended to carefully review changes when working with line-ending conversions.

5. Alternative solutions: While enabling autocrlf is a common approach, there are alternative methods to handle line-ending differences. These include using the .gitattributes file or manually adjusting line endings. Consider the specific needs of your project and choose the approach that best suits your requirements.


----------------------------------------------------------------

# 3. CODING GUIDELINES
- [Clean Code](8https://www.freecodecamp.org/news/clean-coding-for-beginners/)
- [SOLID principles](https://en.wikipedia.org/wiki/SOLID)
- [Angular Styleguide](https://angular.io/guide/styleguide). Main points:
    1. Use a feature-based folder structure instead of a type-based structure.
        -Group related files (components, services, etc.) in the same folder.
        -Use consistent and descriptive naming conventions for files and folders, such as kebab-case for folder names and PascalCase for class names.
    2. Class Naming:
        -Use PascalCase for class names, including components, directives, services, etc.
        -Append the "Component" suffix to component names.
        -Append the "Service" suffix to service names.
    3. Property and Method Naming:
        -Use camelCase for property and method names.
        -Avoid using "get" or "set" prefixes for property accessors.
    4. Template Conventions:
        -Prefix custom attribute names with "ng".
        -Prefix custom component selectors with "app".
    5. Code Organization:
        -Keep code concise and readable.
        -Group imports into separate blocks.
        -Sort imports alphabetically.
    6. Styles Handling:
        -Use Angular's component architecture to apply specific styles to each component.
        -Use SCSS classes for reusable styles and avoid inline styles.
    7. Subscription Management:
        -Unsubscribe from observables in components to prevent memory leaks and unnecessary resource usage.
        -Use takeUntil, unsubscribe operators or DestroyRef to manage subscriptions.
    8. Form Handling:
        -Use the ReactiveFormsModule module for form management.
        -Avoid using ngModel directives in complex forms.
    9. DOM manipulation:
        -Avoid directly manipulating the DOM, use data-binding, Angular built-in directives, ViewChild/ren...
        -For low-level DOM manipulation, use Renderer2
- Languages: use **only English** for the code (you can use other languages for comments)
----------------------------------------------------------------

# 4. STACK

## 4.1 Framework
Angular 16.0.1

## 4.2 Libraries
Try not to overload the project with libraries.
   - Bootstrap: 5.2
   - ngBootstrap: 15.0.0
   - "jasmine-marbles": "^0.9.2",
   - Jest:
        "jest-jasmine2": "^29.5.0",
        "jest-preset-angular": "^13.1.1"
   - JWT: 

----------------------------------------------------------------

# 5. REQUISITES
- Node.js: Make sure you have Node.js installed on your system. You can download it from the official Node.js website.
- Git bash: you will need it  to contribute to the project.

----------------------------------------------------------------

# 6. INSTALLATION
1. Open a terminal or command prompt.
 2. Navigate to the root directory of the project.
3. Run the command 

        npm install
    (or 'npm i') to install all the project dependencies specified in the package.json file.

----------------------------------------------------------------

# 7. DEVELOPMENT
For development purposes, use the command

        ng serve
to start the development server. This will compile the project and serve it locally, enabling you to view and interact with it in your browser.

----------------------------------------------------------------

# 8. TESTING
To run the tests, use the command

    npm test
This will execute the test suite and provide feedback on the test results.
If you prefer to run the tests in watch mode, which automatically re-runs the tests whenever a file changes, use the command

    npm run test:watch.
