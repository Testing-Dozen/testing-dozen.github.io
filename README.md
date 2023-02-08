# Testing Dozen - a Testing Specialist training/mentoring program

**Testing Dozen** is:

* Testing Specialist training / mentoring program run by Maaret Pyhäjärvi, co-facilitated by Mirja Pyhäjärvi
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

![Session4 Concepts](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Session4-Concept.png?raw=true)

Target app:

* <https://chat.openai.com/chat>

Model of testing the session produced:

![Model of testing](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Modeling-ChatGPT.png?raw=true)

Recommended materials:

* [ChatGPT Cheat Sheet](https://drive.google.com/file/d/1UOfN0iB_A0rEGYc2CbYnpIF44FupQn2I/view)

### Session 5: Reproducing bugs based on other people's notes

Targeted Capability:

* Understanding that reporting matters on ease of seeing what you think is a problem
* Reproducing a problem and reporting a problem

Topics:

* Reproduce from other people's notes - why customers reporting and tester's reporting is different
* A sample bug report
* Reproducing from a known list of bugs enables finding bugs outside the list
* Invisible ink of relevant results from testing - usually we don't have a list of bugs but must imagine one
* Bug is anything that might bug a user / other stakeholders

![Sample bug report](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Sample-bug-report.png?raw=true)

Target app:

* [Eprimer app as test target](https://www.exploratorytestingacademy.com/app/)
* [Older version of app as test target](https://maaretp.com/app/)

Listing of what reproduced issues session produced:

![Results with respect to list of known issues, extended](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/bug-list-session5.png?raw=true)

![Results in numbers out of 28 known issues in small groups](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/Repro-60min-result.png?raw=true)

Homework:

* Update statistics on what you could reproduce for next time demo of bugs around the group

### Session 6: Bug Demos and Priorization

Targeted Capability:

* Show and explain a problem
* A tour of all (known) issues
* Prioritizing conversations

Topics:

* Crowdsourcing as practice possibility eg. [Testlio](https://testlio.com), [Utest](https://www.utest.com)) and bug bounties for security bugs esim. [Hackr](https://www.hackr.fi)
* Ensure everyone in group has seen and understood the versatility of "bugs"
* Bugs as anything that might bug a user - improvement suggestions, missing features, implementation mistakes
* Research while testing, grounding with priority: fixing relevance of the project
* Completing round of problems with this application

 [Bug list of known symptoms, new identified symptoms and cleaning up to a little clearer list and bug reports.](eprimer_buglist.md)

 ![Results with respect to list of known issues, extended with bugs demoed student-driven](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/bug-list-session6.png?raw=true)

### Session 7: WebApps with APIs

Targeted Capability:

* Listing functionalities not only bugs
* Analysis: function and structure

Topics:

* Ensemble exploratory testing, emergent constraints
* Functionality and bug note listing
* Local and hosted test environments
* Intro to REST APIs
* Debugging in IDE
* Python requests library

Target App:

* Restful Booker Platform by Mark Winteringham
  * [Code and java test samples](https://github.com/mwinteringham/restful-booker-platform]
  * [Hosted test version with limitations](https://automationintesting.online)
* Our ensemble notes [https://github.com/Testing-Dozen/dozen_restful_booker](https://github.com/Testing-Dozen/dozen_restful_booker)

Recommended materials:

* [Video on exploratory testing of *this* API](https://www.youtube.com/watch?v=FfGQX6cSf6o)
* [Mark's book, Testing Web APIs](https://www.amazon.com/Testing-Web-APIs-Mark-Winteringham/dp/1617299537)

Homework:

* Inspect in browser, network tab and requests and responses

### Session 8: GET Endpoint with 200 response and contents

Targeted Capability:

* First basic API test for GET endpoint on local and remote deployments

 Topics:

* Localhost and hosted on some computer (cloud) deployments
* Unauthenticated endpoints with requests-library
* GET and 200 response, verifying whole, contains, element contains and element exists conditions
* Setup and teardown with pytest fixtures

Target App:

* Restful Booker Platform by Mark Winteringham

![Concepts](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/session8.png?raw=true)

Our Tests:

* [https://github.com/Testing-Dozen/dozen_restful_booker](https://github.com/Testing-Dozen/dozen_restful_booker)

Homework:

* Create GET and POST calls on the front page APIs that are unauthenticated

### Session 9: Strengthen pytest foundations

Targeted Capability:

* Exploratory unit testing applied on roman numerals function beyond most obvious tests

Topics:

* Applying positions as trainee / junior test engineer
* pytest foundations: test naming, asserts, approvals, parametrizing, conftest
* Testing fundamentals: coverage, results, oracles

Target App:

* Github Copilot generated roman numerals function
* Available at lines 1-16 on [https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/blob/main/important_program.py](important_program.py)

Our tests:

* [https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/](https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/)

Homework:

* Study traditional and simplified roman numerals in excel
* Review code for [Excel and Know the Romans -page reference implementations](https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/tree/main/helpers)

Recommended Readings:

* [How to Make Your VSCode Sparkle](https://aboutmonica.com/blog/how-to-make-your-vs-code-sparkle/)
* VSCode extensions: [Mermaid theme](https://marketplace.visualstudio.com/items?itemName=StephKeys.mermaid-theme)
* VSCode extensions: [Power mode](https://marketplace.visualstudio.com/items?itemName=hoovercj.vscode-power-mode)

### Session 10: ApprovalTests, SoftAssertions, Snapshots and Properties

Targeted Capability:

* Using earlier tests to remember earlier testing
* Test styles beyond examples of asserts

Topics:

* ApprovalTests - Run (red), Approve, Run (green), and combinationapprovals
* SoftAssertions - Collating multiple assertion results instead of failing on first
* Snapshots - Run (save), Run (green), fail when output changes
* Properties, hypothesis library - programmatic rules, generated falsifiable hypothesis tests
* xfail-decorator - expecting a failure

Target App:

* Github Copilot generated roman numerals function
* Available as [https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/blob/main/important_program.py](important_program.py)

Our tests:

* [https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/](https://github.com/exploratory-testing-academy/do-a-thing-and-call-it-foo-solution/)

![24 tests](https://github.com/Testing-Dozen/testing-dozen.github.io/blob/main/session10-results.png?raw=true)

Recommended Reading:

* [What is ApprovalTesting](https://www.methodsandtools.com/archive/approvaltest.php)

Homework:

* Study restful booker API testing project current state

### Session 11: From GET to POST and PUT

Targeted Capability:

* Running containerized local environment
* Creating and using pytest fixtures
* GET, POST, PUT and authentication in cookies

Topics:

* Starting with someone else's python test project, setting virtual environment and installing dependencies
* Authenticated endpoints with requests-library using pytest fixtures
* GET, POST, PUT and 200 vs. 400 response
* 'docker-compose up' and 'docker-compose down' to run test target on localhost

Target App:

* Restful Booker Platform by Mark Winteringham
* Code: [https://github.com/mwinteringham/restful-booker-platform](https://github.com/mwinteringham/restful-booker-platform)

Our Tests:

* [https://github.com/Testing-Dozen/dozen_restful_booker](https://github.com/Testing-Dozen/dozen_restful_booker)


Homework:

* Pull requests adding more tests for restful booker APIs

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
