Step-1:
I set up the provided Python application in a GitHub Codespace and created a virtual environment for the project. The required dependencies, pytest, and coverage tools were installed successfully. I then ran the existing unit tests with pytest --cov=src --verbose to verify the application and review its current test coverage.

The test results helped establish a baseline for the project's automated testing before adding GitHub Actions workflows in the next step.

Step-2:
I added GitHub Actions workflows to automate testing and code coverage. The Python test workflow runs the test suite whenever changes are submitted through a pull request to the main branch. I also added a separate coverage workflow that runs the tests with pytest-cov and reports the code coverage directly on the pull request.

This helps catch issues early(automatically). The workflow was successfully executed through GitHub Actions, confirming that the automated testing setup is working as expected.