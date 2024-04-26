# playwright-sample-with-ci

This is a simple demonstration project to show how **Playwright** framework works with **GitHub CI**, built using **Javascript** and **Playwright**.

## Installing

These instructions will help you download the project onto your local machine.

1. Download and install a **Node.js** environment from this [site](https://nodejs.org/en/) (version 20.9.0 or higher).

2. Download the repository to your local machine using the **Command Prompt** command:

```
git clone https://github.com/zefirlover/playwright-sample-with-ci.git
```

> [!NOTE]
> **PLEASE BE AWARE** that the project will be downloaded into the folder where the **Command Prompt** was opened. Be sure to start the **Command Prompt** from the folder where you want to place the repository, or navigate there using the [`cd` command](https://learn.microsoft.com/uk-ua/windows-server/administration/windows-commands/cd).

3. Navigate to the project directory and open it using **Visual Studio Code** (or any other desktop code editor capable of working with **Javascript**).

4. Open the terminal (for VSCode, use the **Ctrl + Shift + `** hotkeys or select *Terminal > New Terminal from the navigation menu*). After that, to install all the dependencies, run:

```
npm i
npm init playwright@latest
```

5. *(optional)* To run tests with **allure-reporter** locally you need to install **Java v.8** or above on your machine. **PLEASE MAKE SURE** that Java directory is specified in the `JAVA_HOME` environment variable.

> [!NOTE]
> You can run these commands using the **Command Prompt** opened in the project folder.

## How to start your tests

Currently, the only way to run your tests is by using [**Playwright** commands](https://playwright.dev/docs/running-tests). Here is a list of possible commands to do just that:

- To run tests in headless mode:
```
npx playwright test
```
- To run them in headed mode:
```
npx playwright test --headed
```
- To run in UI mode:
```
npx playwright test --ui
```
- To run a specific spec:
```
npx playwright test example.spec.js
```
- To run tests with **allure** reporter:
```
npx playwright test --reporter=line,allure-playwright
```
- To generate report:
```
npx allure generate --clean
```
- To open report locally:
```
allure serve
```

## Build with

- [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) - a lightweight interpreted programming language with first-class functions, that used for this project
- [Playwright](https://playwright.dev/) - a cross-browser, cross-platform and cross-language framework that can be used for Web, API and mobile (to some degree) automation testing
- [Allure](https://allurereport.org/) - a reporter that is used to create and show tests reports for the test runs
