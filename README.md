# Expo CLI Error: Native Module Not Found or Not Properly Linked

This repository demonstrates a common error in Expo CLI projects when using packages that require native modules. The error typically arises from incorrect package installation or linking, leading to undefined or unavailable native modules during runtime.  The solution focuses on verifying the package installation, and confirming it is properly linked.

## Steps to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Attempt to run the app using `expo start`.  Observe the error related to a missing native module. 
4. Follow the instructions in `bugSolution.js` to resolve the issue.

## Solution

The solution involves verifying proper package installation and linking.  This may include:

* **Reinstalling the package:**  Use `expo install <package-name>` to reinstall the package, ensuring a clean installation.  Check the package's documentation for specific instructions.
* **Checking for linking issues:** Some packages require manual linking.  Consult the package's documentation for any necessary linking steps.  If the package uses Expo's managed workflow, ensure there aren't any conflicts.
* **Resolving version conflicts:** If you have conflicting versions of packages (especially native modules), try using `expo prebuild` to resolve potential compatibility issues.  Review your `package.json` for potential version conflicts. 
* **Cleaning the project:** Try cleaning the project's cache: `expo prebuild --clean`