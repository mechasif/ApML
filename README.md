# ApML
Getting started with ESP-EYE and Machine Learning


## Installation Issue

**ERROR: The following Python requirements are not satisfied: Requirement 'pyparsing<2.4.0,>=2.0.3' was not met. Installed version: 3.x.x**

**Error indicating a mismatch between required and installed versions of the `pyparsing` library.**

To solve this:

1. **Activate the ESP-IDF Python Environment**:

   Before modifying the Python environment, you need to activate the specific environment used by ESP-IDF.

   ```bash
   source YourDirectory/python_env/idf4.4_py3.10_env/bin/activate
   ```

2. **Downgrade the `pyparsing` Version**:

   You need to downgrade `pyparsing` to a version that fits the requirements:

   ```bash
   pip install pyparsing==2.3.1
   ```

3. **Re-run the ESP-IDF Installation Script**:

   Sometimes, it's good to re-run the provided ESP-IDF installation script after manually resolving dependency issues. This ensures that all other dependencies are in place:

   ```bash
   YourDirectory/esp-idf/install.sh
   ```

4. **Verify the `pyparsing` Version**:

   Confirm that you now have the correct version of `pyparsing`:

   ```bash
   pip list | grep pyparsing
   ```

   It should display a version in the range >=2.0.3 and <2.4.0.

5. **Deactivate the ESP-IDF Python Environment**:

   After you're done, remember to deactivate the ESP-IDF's Python environment:

   ```bash
   deactivate
   ```

