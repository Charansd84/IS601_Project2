Heroku App Link - https://project1lasttry.herokuapp.com/

[![Production Workflow] (https://github.com/Charansd84/IS601_Project2/blob/master/.github/workflows/prod.yml) }]

* [Production Deployment] (https://is601newproject2.herokuapp.com/)


[![Development Workflow] (https://github.com/Charansd84/IS601_Project2/blob/master/.github/workflows/dev.yml)]

* [Developmental Deployment] (https://is601newproject2.herokuapp.com/)

## Project files
docker_flask <- root of the project .github

workflows <- contains the yml files for proper workflow of authorized user
dev.yml <- projects development workflow
prod.yml <- projects production workflow

.pytest_cache <- offer a mechanism through which other plugins can get/set values via config.cache.get|set. This is used by pytest-pep8 and pytest-flakes for example to store the mtime of the last check to avoid re-checking files all the time.
The default cache directory has been renamed from .cache to .pytest_cache after community feedback that the name .cache did not make it clear that it was used by pytest.

cache <- directory containing the cache files

lastfailed <- The plugin provides two command line options to rerun failures from the last pytest invocation: --lf , --last-failed - to only re-run the failures. --ff , --failed-first - to run the failures first and then the rest of the tests.

nodeids <- The node ids in pytest are built of several components, separated by a double colon “::”. For test functions, these components are the relative path of the test module and the name of the function.cache file of node id
stepwise <- pytest-stepwise is a plugin for pytest that run all tests until a test fails, and then continue next test run from where the last run failed.
.gitignore <- The .gitignore file tells Git which files to ignore when committing your project to the GitHub repository.

CACHEDIR.TAG <- Only one cache directory tag is required to tag an entire subdirectory tree of cached content. The application should also regenerate the cache directory tag if it disappears: e.g., if the entire contents of the cache directory is deleted without the directory itself being deleted.

README.md <- text file explaining .pytest_cache directory.

app <- contains all html, css and javascript files

context_processors <- To inject new variables automatically into the context of a template, context processors exist in Flask. Context processors run before the template is rendered and have the ability to inject new values into the template context. A context processor is a function that returns a dictionary.
__init__.py <- the Flask application object creation has to be in the __init__.py file. That way each module can import it safely and the __name__ variable will resolve to the correct package.
simple_pages <- simple pages are not item pages and are not dynamically generated. They are free-standing pages that you construct using an editor box that allows you to write text, insert images, and even embed videos.
templates
about.html <- information about the web application
index.html <- main page
page1.html <- information about git (merge, commit, branching)
page2.html <- information about docker
page3.html <- information about flask
page4.html <- Continuous Integration and Deployment

__init__.py <- a function that renders, locates and returns pages stored in simple_pages/templates.
static <- a directory that has images, css and javascript files.
css <- directory containing css files
style.css <- style sheet for html files
images <- directory of images used in web application
js <- directory with javascript files
scripts.js <- javascript file
templates <- contains the base html file for the web application
base.html <- base file for all html pages

__init__.py <- Create and configure an instance of the Flask application.
run.py <- This allows Gunicorn to serve the app in production
calculator <- directory with calculator related python files
__init__.py <- class for calculator calculations
tests <- directory containing test files for github action
__init__.py <- instance of tests

calculator_test.py <- test to check calculations

conftest.py <- test configuration setup

context_process_test.py <- checks for printing copyrights and environment
simple_pages_test.py <- test to check if all documents simple_pages are correctly displayed
.coveragerc <- it's a tool for measuring code coverage of Python programs. It monitors your program, noting which parts of the code have been executed, then analyzes the source to identify code that could have been executed but was not. Coverage measurement is typically used to gauge the effectiveness of tests.
.dockerignore <- it allows you to exclude files from the context like a . gitignore file allow you to exclude files from your git repository. It helps to make build faster and lighter by excluding from the context big files or repository that are not used in the build.
.gitignore <- it tells Git which files to ignore when committing your project to the GitHub repository. gitignore is located in the root directory of your repo. The .gitignore file itself is a plain text document.
.pylintrc <- it is a tool that checks for errors in Python code, tries to enforce a coding standard and looks for code smells. It can also look for certain type errors, it can recommend suggestions about how particular blocks can be refactored and can offer you details about the code's complexity.
docker-compose.yml <- Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application's services. Then, with a single command, you create and start all the services from your configuration
Dockerfile <- A text document that contains all the commands a user could call on the command line to assemble an image. Using docker build users can create an automated build that executes several command-line instructions in succession.
heroku.yml <- A configuration file for heroku server
pytest.ini <- is the main configuration file of pytest, which can change the running mode of pytest. It is a fixed file, read the configuration information, and run in the specified way.
readme.md <- contains a few explanations to run the project for yourself
requirements.txt <- A type of file that usually stores information about all the libraries, modules, and packages in itself that are used while developing a particular project. It also stores all files and packages on which that project is dependent or requires to run.
setup.py <- A python file, the presence of which is an indication that the module/package you are about to install has likely been packaged and distributed with Distutils, which is the standard for distributing Python Modules. This allows you to easily install Python packages.

## Setting up CI/CD

Continuous Integration and Deployment
Continuous integration is a step in which all code is merged as developers complete code in order to run automated builds and tests. Continuous deployment is the process of moving software that has been built and tested successfully into production. Automated tests verify the software functionality, and automated deployment services deliver them to end users. This helps developers discover bugs and defects faster and increases productivity and faster release cycles.


Continuous integration: is a DevOps software development practice where developers regularly merge their code changes into a central repository, after which automated builds and tests are run.

Continuous Deployment: is a software release process that uses automated testing to validate if changes to a codebase are correct and stable for immediate autonomous deployment to a production environment.
Note
Continuous Delivery is sometimes confused with Continuous Deployment. Continuous Deployment means that every change goes through the pipeline and automatically gets put into production, resulting in many production deployments every day. Continuous Delivery just means that you are able to do frequent deployments but may choose not to do it, usually due to businesses preferring a slower rate of deployment. In order to do Continuous Deployment you must be doing Continuous Delivery.

- > In your newly created Github repository, add new repository secrets for DOCKER_USERNAME, DOCKER_PASSWORD, HEROKU_API_KEY (Values are DOCKER_USERNAME: your docker hub username; DOCKER_PASSWORD: your docker hub password; HEROKU_API_KEY: API key from the heroku app)
### GitHub Notes:  Set the action secrets repository in: -> settings -> actions -> secrets
### Heroku Notes: Get the heroku API key from account in: -> applications -> create authorization button

## Running Locally

1. To Build with docker compose:
   docker compose up --build
2. To run tests, Lint, and Coverage report use this command: pytest --pylint --cov

