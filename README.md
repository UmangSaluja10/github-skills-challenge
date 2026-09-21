Step-1:
I set up the provided Python application in a GitHub Codespace and created a virtual environment for the project. The required dependencies, pytest, and coverage tools were installed successfully. I then ran the existing unit tests with pytest --cov=src --verbose to verify the application and review its current test coverage.

The test results helped establish a baseline for the project's automated testing before adding GitHub Actions workflows in the next step.

Step-2:
I added GitHub Actions workflows to automate testing and code coverage. The Python test workflow runs the test suite whenever changes are submitted through a pull request to the main branch. I also added a separate coverage workflow that runs the tests with pytest-cov and reports the code coverage directly on the pull request.
Step-3:

This helps catch issues early(automatically). The workflow was successfully executed through GitHub Actions, confirming that the automated testing setup is working as expected.

A separate reenable-unit-test branch was created from main to demonstrate the pull-request based workflow. A previously disabled Fibonacci unit test was re-enabled and the changes were pushed to GitHub. A pull request was then created targeting the main branch, which automatically triggered the configured GitHub Actions workflows.

The test workflow and coverage workflow ran against the pull request, allowing the results to be reviewed directly from GitHub. This demonstrated how pull requests can be used to automatically validate changes before they are merged.

Step-4: 
Branch protection was added to the main branch using a ruleset named Protect main. The python-coverage status check was made mandatory before changes could be merged. This prevents code from being merged when the required verification workflow fails.

During validation, the re-enabled Fibonacci test was found to contain an incorrect expected value. The test originally expected 89 for the 10th Fibonacci value, so it was corrected to 55. After fixing the test, the remaining issue was insufficient test coverage.