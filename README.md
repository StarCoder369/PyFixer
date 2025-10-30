PyFixer - AI-Powered Python Code Analyzer

Instructions:
-------------
Follow these steps carefully. This will set up PyFixer and allow you to run it on your own Python projects.

Step 1: Install Python and Pip
- Make sure Python 3.8 or higher is installed on your system.
- MacOS: Open Terminal and type:
      python3 --version
  You should see the Python version.
- Windows: Open Command Prompt (press Win + R, type cmd) and type:
      python --version
  If it shows a version, Python is installed. If not, download and install from python.org.

Step 3: Navigate to the downloaded PyFixer.zip folder
- This should look something like: "PyFixer-main.zip"

Step 4: Unzip all necessary files
- Double click to unzip PyFixer-main.zip.
- When opened, a zip file named: "PyFixer.zip" should show up
- Unzip this file too.

Step 5: Open terminal through the file
- Right click on PyFixer.zip, and click New Terminal At Folder.
  
Step 6: Install dependencies
- Type the following command to install all required Python packages:
      pip install -r requirements.txt
- This installs Pylint and Requests, which PyFixer needs to work.

Step 7: Install PyFixer as a package
- Type:
      pip install '-e.' Remember to add the period at the end of the command.
- The `-e` flag installs it in "editable" mode. This means you can update PyFixer files and still run it without reinstalling.

Step 8: Install Ollama AI and pull the model
- PyFixer uses Ollama for AI analysis.
- Make sure Ollama is installed and running:
      ollama status
- Pull the AI model PyFixer uses:
      ollama pull granite-code:3b
- Wait until the model is fully downloaded.

Step 9: Go to your Python project folder
- Navigate to the project you want to scan or analyze:
      cd path/to/your/project
- Example:
      cd /Users/YourName/Documents/MyPythonProject   (Mac)
      cd C:\Users\YourName\Documents\MyPythonProject (Windows)

Step 10: Run PyFixer
- Simply type:
      pyfixer
- Press Enter.
- This will launch PyFixer’s menu.

Main Menu Options:
------------------

Please note: Whenever asked for the path of a file, this is how you get it.

Mac: Navigate to the file you want to copy the path of in the finder. Right click on the file, then hold the option key, where an option to copy as pathname will show up. Click on that, then paste it.

Windows: Navigate to the file. Shift + Right Click the file, select copy as path. Paste it.

If on PyCharm: Find the file you want to copy the path of, right click on it, then click copy path reference, Absolute Path. Now you can paste it.

[1] Static Code Scan
    - Checks all Python files in the inputted path using Pylint.
    - Finds potential bugs, style issues, and anti-patterns.

[2] AI Module
    - Provides AI-assisted code review and Q&A.
    - After selecting, you get:
      [1] Analyze a single Python file
          - Type the path to the Python file you want to analyze.
          - AI will read it and suggest fixes for bugs or logic issues.
      [2] Ask a general code question
          - Ask anything related to Python coding.
          - AI does not scan the full project automatically.
      [3] Exit AI Module
          - Returns to main menu.

[3] Exit
    - Closes PyFixer.

Notes:
------
- Make sure Ollama is running locally whenever you want to use the AI module.
- Static scans run entirely locally and are fast.
- AI analysis may take a few seconds depending on the file size.
- If PyFixer is not recognized:
      - Ensure you installed it with `pip install -e .`
      - Check that Python is added to your system PATH.
- If Python is not recognized:
      - Mac: Python 3 usually comes preinstalled; otherwise, install from python.org
      - Windows: Install Python 3 from python.org and check "Add Python to PATH" during installation
