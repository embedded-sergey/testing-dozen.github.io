# Testing Dozen - a Testing Specialist training/mentoring program

**Testing Dozen** is:
  * Testing Specialist training / mentoring program run by Maaret Pyhäjärvi
  * In Finland for people seeking testing jobs in Finland
  * Pilot batch runs 6 months from November 16th, 2022

## Participants
  * Aino
  * Svetlana Egorov @SvetlanaS1212
  * Pia @piavesala
  * samuel @samuelnarteyGH @samuelnomis
  * Miia @iammiiam
  * Olga Larintseva @Loranpire
  * Katri Kiero @katrikiero
  * Gold Lola @GoldLola
  * Olayinka  @Olayinka_Dele
  * Hanna @tuutin-t
  * Sanna Tawah @nanahamjam
  * Martha  @Lopezmartha
  * Sergey   @embedded-sergey
  
## Sessions as those emerge

### Session 1: Introductions and Github portfolio starter

What we did:
  * Create 1st version of this page on Github
  * Remote control tech check: writing names over Zoom remote control on this page on Maaret's computer
  * Making changes through forks, branches and pull requests

Targeted Capability:
   * Place for creating portfolio of your learning - your Github
   * Linking your Github with course page
   
Topics:
  * Github: repositories, forks and branches, pull requests

![Concept summary](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Session1-concepts.png?raw=true)

Homework: 
  * Improve this page through pull requests
  * Install Git and VSCode
  
Recommended reading:
  * [Git tutorial](https://www.w3schools.com/git/)
  * [Markdown manual](https://www.markdownguide.org/basic-syntax/) 
  * [Catalin Pit: How to Create a Kickass GitHub Profile Page](https://catalins.tech/how-to-create-a-kickass-github-profile-page/)
  * [Ship, show ask - branching strategies](https://martinfowler.com/articles/ship-show-ask.html)

### Session 2: Automationist's Gambit

Targeted Capability:
  * Writing basic tests for a web app with Python and Playwright
  * Exploring through automation to find bugs
  
Topics:
  * Contemporary exploratory testing with automationist's gambit
  * Basic concepts: bug, test, coverage, oracle, heuristics
  * Basic Python, pytest and Playwright

![Concept summary](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Session2-concepts.png?raw=true)

Target app:
  * [Eprimer app as test target](https://www.exploratorytestingacademy.com/app/)
  * [Test Code Repo for ETF course](https://github.com/exploratory-testing-academy/ETF)
  * [Python-pytest-playwright commands ReadMe](https://github.com/exploratory-testing-academy/ETF/blob/master/python-playwright/README.md)

Gist of what session produced:
  * [Gist of session 2 tests](https://gist.github.com/maaretp/cfd3a9097abbefd7cb9683d6f9e26dec)
  
Homework: 
  * Try to get python-pytest-playwright tests to run on your computer
  * Think about more inputs that could reveal bugs

Recommended readings: 
  * [Courseware: Exploratory Testing Foundations -course](https://dev.to/maaretp/exploratory-testing-foundations-4lb3)
  * [pytest](https://docs.pytest.org/en/7.2.x/)
  * [playwright in python](https://playwright.dev/python/docs/intro)
  * [Top Programming Languages 2022](https://octoverse.github.com/2022/top-programming-languages)
  * [Elisabeth Hendrickson: Test Heuristics Cheat Sheet](https://drive.google.com/file/d/1TaFRhTsy0QRjgtaHSVu3L73Q9JVee0hA/view?usp=sharing)
  * [Github Naughty Strings](https://github.com/minimaxir/big-list-of-naughty-strings)
  * [Exploratory Testing Dynamics](https://www.developsense.com/resource/et-dynamics3.pdf)
  * [QA Engineer Roadmap - conceptual learning map](https://roadmap.sh/qa)
  * [Computing tools for CS studies course material](https://tkt-lapio.github.io/en/)

### Session 2.1 - Installing your dev environment

Checklist to get tooling installed:
  * install vscode (win/mac: download and install) -> see it starts
  * verify what is installed from vscode terminal: `git --version`, win: `python --version`, mac `python3 --version`, `node --version`
  * install tooling managing programmer tooling on mac: homebrew
  * install tooling: git (win: download&install, mac: `brew install git`)
  * install programming languages: python (win: download&install, mac: `brew install python3.11`)
  * install programming languages: nodejs (win: download&install, mac: `brew install node`
  * verify what is installed from vscode terminal: `git --version`, win: `python --version`, mac `python3 --version`, `node --version`

Checklist for further configuring tooling:
  * add local folder and open folder in vscode
  * change terminal on windows: git bash or cmd over powershell
  * add simple file.py with `print('whatever')` in it and run it from terminal with `python file.py`
  * sandbox your folder as python virtual environment with `python -m venv .venv`
  * activate your virtual environment (win: restart terminal, mac: `source .venv/bin/activate`
  * install dependencies: pytest (win/mac: `pip install pytest`)
  * create simple test_file.py with one test method `def test_method(): pass` 
  * run tests from terminal with `pytest test_file.py`
  * define pytest as test framework for test lab in vscode to see test_files and test_method() in runner
  * create requirements.txt file and write in dependencies, each on own line: `pytest`, `playwright`, `pytest-playwright`
  * install repo dependencies based on requirements.txt with `pip install -r requirements.txt` on terminal
  * install playwright node tooling with `playwright install on terminal
  * clone a project from github and open that folder in vscode, sandbox with virtual environment as before
  * make changes in files, try commit&sync in vscode
  * to commit successfully, define git.name and git.email from terminal [how to](https://linuxize.com/post/how-to-configure-git-username-and-email/)
  * to sync successfully, create keys for github access on git bash [how to](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Extra practice:
  * learn to navigate folders with `cd ..` and `cd folder_name` and check files in folder with win: `dir`, mac: `ls` / `ls -la`
  * learn to use autocomplete - write only max 3 letters and allow tab to autocomplete
 
Extra test playwright operational without sample project:
  * create test_playwright.py -file with `from playwright_sync_api import Page` and `def test_pw(page: Page):` and `page.goto("https://exploratorytestingacademy.com")` each on own line as the skeleton test case
  * run tests `pytest --headed test_playwright.py`
  * create pytest.ini -file with contents `[pytest]` and `addopts = --headed --browser chromium --slowmo 2000` to continuously run tests showing the browser, using chromium and slowing steps by 2 seconds

### Session 3: Discovering information

Targeted Capability:
  * Extending inputs to find bugs
  * Increased comfort with editing automated tests to extend with data samples
  
Topics:
  * Testing as discovery
  * Basic pytest-bdd in gherkin + pytest + playwright
  * Bug and other words that mean almost the same

![Concept summary](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Session3-concepts.png?raw=true)

Target app:
  * [Eprimer app as test target](https://www.exploratorytestingacademy.com/app/)

Gist of what session produced:
  * [Gist of session 3 tests](https://gist.github.com/maaretp/3fa7ac39b5ef33c0c48f9184bd201c81)
  
Homework: 
  * Think about how to reveal more bugs - preview 'known bugs' and think about how you could find them

![Known Bugs](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Known-Bugs.png?raw=true)

Recommended readings: 
  * [Playwright API](https://playwright.dev/python/docs/api/class-playwright) 
  * [James Lyndsay's Raster Reveal](https://www.workroom-productions.com/raster-reveal/)
  
### Session 4: Black-box testing AI text generator

Targeted Capability:
   * Learning about an entirely different type of system (text generator not a search engine) 
   * High level idea of ML in software systems

Topics:
   * Black-box testing
   * Modeling, inputs and outputs
   * Test environment, test target readiness / availability
   * Exploratory testing, scale from technique to approach
   
![Black-Box Testing](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/BlackBoxTesting.png?raw=true)


Target app: 
   * https://chat.openai.com/chat
   
Model of testing the session produced: 

![Model of testing](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Modeling-ChatGPT.png?raw=true)


## Targeted Skills

Can do the testing job? 

  * Can look at an application and make sense of it
  * Can create UI and API tests on it (using programming language)
  * Can structure test code so that reading them make sense for later
  * Can define epics acceptance criteria
  * Can ask good questions about features
  * Can suggest ways to improve testability
  * Can make sense and extend pipelines
  * Can analyze changes
  * Can define experiments
  * Can fail gracefully with pride of learning
  * Can actively learn useful things
  * Can apply good judgement, prioritise and decide
  * Can install software on various OSs, configure and operate it
  * Can say when they are unsure and actively seek understanding
  * Can create models and use them to derive coverage
  * Can communicate results and status 
  * Can figure out systems of systems impact on testing
