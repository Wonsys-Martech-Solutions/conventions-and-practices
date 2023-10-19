# Table of Contents
1. [Introduction](#introduction)
2. [Technology Stacks](#technology-stacks)
3. [Coding Standards](#coding-standards)
   - [Consistent Code Formatting](#cosistent-code-formatting)
   - [Variable Naming Conventions](#variable-naming-conventions)
   - [URL / API Path Conventions](#url--api-path-conventions)
   - [TypeScript](#typescript)
4. [Version Control](#version-control)
   - [Version Control System Overview](#version-control-system-overview)
   - [Git Best Practices](#git-best-practices)
   - [Branching Strategies](#branching-strategies)
   - [Commit Message Guidelines](#commit-message-guidelines)
   - [Handling Merge Conflicts](#handling-merge-conflicts)
   - [Best Practices for Collaborative Version Control](#best-practices-for-collaborative-version-control)
5. [Pull Request Workflow](#pull-request-workflow)
   - [Creating and Managing Pull Requests](#creating-and-managing-pull-requests)
   - [Code Review Guidelines](#code-review-guidelines)
6. [Collaboration Guidelines](#collaboration-guidelines)
   - [Effective Communication within Development Teams](#effective-communication-within-development-teams)
   - [Code Review Etiquette](#code-review-etiquette)
   - [Collaborative Tools and Practices](#collaborative-tools-and-practices)
7. [Localization and Internationalization (i18n)](#localization-and-internationalization)
   - [Preparing for Localization in Software](#preparing-for-localization-in-software)
   - [Managing Translations and Multilingual Content](#managing-translations-and-multilingual-content)
   - [Internationalization Strategies and Best Practices](#internationalization-strategies-and-best-practices)
8. [Project Structure](#project-structure)
   - [Directory Structure and Organization](#directory-structure-and-organization)
   - [Modular Code Design and Componentization](#modular-code-design-and-componentization)
9. [Code Review](#code-review)
   - [Code Review Processes and Workflows](#code-review-processes-and-workflows)
   - [Conducting Effective Code Reviews](#conducting-effective-code-reviews)
   - [Code Review Checklists and guidelines](#code-review-checklists-and-guidelines)
   - [Benefits of Code Reviews for Code Quality](#benefits-of-code-reviews-for-code-quality)



## Introduction
Welcome to Wonsys Github repository! This document outlines the ***conventions and best practices*** we follow to maintain consistency and efficiency in our development workflow. Whether you're a Full Time, Part Time, Freelancer or even an Intern, adhering to these convetions will make collaboration smoother and codebase management more manageable.

## Technology Stacks
**Frontend**
1. [React.js](https://react.dev/)
2. [Next.js](https://nextjs.org/)
3. [@tanstack/react-query](https://tanstack.com/query/latest)
4. [TypeScript](https://www.typescriptlang.org/)
5. [Tailwind CSS](https://tailwindcss.com/)

**Backend**
1. [Node.js](https://nodejs.org/en)
2. [Express.js](https://expressjs.com/)
3. [Nest.js](https://nestjs.com/)
4. [TypeScript](https://www.typescriptlang.org/)
5. [Prisma](https://www.prisma.io/)

## Coding Standards
We follow a set of coding standards to ensure that our code is readable, maintainable, and consistent across the repository. These standards cover aspects such as code formatting, variable naming conventions, and more. Make sure to review our [Coding Standards](#coding-standards) document for detailed guidelines.

### Consistent Code Formatting
To ensure standardized code styling while using [VS Code](https://code.visualstudio.com/), it is recommended that you install the [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) plugin. Once installed, you can maintain consistent code formatting. Additionally, don't forget to copy the [.prettierrc](https://github.com/Wonsys-Martech-Solutions/conventions-and-practices/blob/main/.prettierrc) configuration file to your project.
```json
{
  "singleQuote": true,
  "tabWidth": 4,
  "trailingComma": "es5",
  "printWidth": 150,
  "semi": true,
  "bracketSpacing": true
}
```

### Variable Naming Conventions
When naming variables, it's essential to use descriptive and meaningful names that convey the purpose and content of the variable. Follow a consistent naming convention, such as ***camelCase***, ***snake_case***, or ***PascalCase***, depending on your programming language and project guidelines.

***Best Practice:***
1. ***Use Descriptive Names:*** Choose variable names that clearly describe the data they hold or the purpose they serve in the code. Avoid single-character names or overly cryptic abbreviations.
    ```js
    # Not Recommended
    const x = 10
    const y = "John"

    # Recommended
    const age = 30
    const firstName = "John"
    ```
    
2. ***Avoid Ambiguity:*** Variable names should not be ambiguous or misleading. A variable's name should make its purpose evident to other developers reading the code.
   ```js
   # Ambiguous
   const data = [
       {
           name: "John",
           age: 21
       }
   ]

   # Clear and specific
   const employee = [
       {
           name: "John",
           age: 21
       }
   ]
   ```

### URL / API Path Conventions
URL / API path naming should not contain uppercase and spacing (Replace spacing with `-`). No Verbs in the URL / API path allow:
   ```
   # Not Recommended
   1. https://example.com/user/1/activityLog
   2. https://example.com/user/1/activityLog/update

   # Recommended
   1. https://example.com/user/1/activity-log
   2. https://example.com/user/1/activity-log (use PUT Request Instead)
   ```

### TypeScript
TypeScript's real power lies in its strong type system, which helps catch errors early, improve code quality, and enhance codebase maintainability. To maximize these benefits, it's essential to avoid using the `any` type and strive to put types everywhere. Here's a best practice for achieving this:

***Avoid Using `any` Type:***
`any` is a TypeScript type that effectively disables type checking for a variable, allowing it to store any value. Although it can be tempting for rapid development, it compromises TypeScript's primary objective. To encourage a type-safe codebase:
   
- **Minimize the Use of `any`:**
  
  Try to minimize the use of `any`, unless you have a compelling and well-documented reason, such as when interfacing with untyped third-party libraries. When employing any, you forfeit the advantages of static typing.
  
- **Enable the `noImplicitAny` Compiler Option:**
  
  In your tsconfig.json file, set `"noImplicitAny": true`. This setting will enforce strict typing, discouraging the application of `any`, and highlighting any implicit `any` types in your codebase during compilation.
  
- **Clearly Define Types:**
  
  Instead of depending on `any`, clearly define types for variables, function parameters, states, and return values. TypeScript provides a rich selection of built-in types, and you can craft custom types or interfaces to accurately represent specific data structures.




[Creating a Git Commit Message Convention](https://medium.com/@naandalist/creating-a-git-commit-message-convention-for-your-team-acb4b3edfc44)

dev - development (eg: a new feature)
fix - fixing some bug
refactor - revamp or redo something
<type> (<scope / module>) - <subject>
dev (course) - adding course table 

