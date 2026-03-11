AI Usage Log - Lab 0
Interaction 1: Git Repository Initialization

1. Context: Setting up the local project folder and linking it to an empty GitHub repository without uploading unnecessary files.

2. Prompt(s): "How to properly initialize a local folder and link it to an empty GitHub repository"

3. Relevant Output: Step-by-step terminal commands (git init, git remote add, git branch -M main) and folder structure corrections to avoid nested repos.

4. Validation: Executed the commands in the VS Code terminal and verified via the GitHub web interface that the files were pushed correctly, confirming the .venv folder was successfully ignored by .gitignore.

5. Adaptations: None. I used the exact terminal commands provided by the AI.

6. Final Decision: Used. It established a clear and organized Git hierarchy, solving my initial fatal: not a git repository error.

Interaction 2: Windows Path Length Limit (pip install error)

1. Context: Creating a reproducible Python environment locally on Windows using requirements.txt and encountering a file path system error.

2. Prompt(s): "How to resolve [Errno 2] No such file or directory during pip install when setting up requirements.txt in Windows"

3. Relevant Output: Identified the Windows 260-character path limit (Long Paths issue) and provided a minimal, version-pinned requirements.txt along with a PowerShell registry fix.

4. Validation: I verified the existence of the MAX_PATH limitation in Windows documentation. After running the PowerShell command, I tested the environment creation again to ensure it didn't crash.

5. Adaptations: Replaced my bloated, auto-generated requirements.txt with the minimal 9-package version  (pinning major.minor versions as required by the rubric).

6. Final Decision: Used. It solved a critical OS blocker that prevented the creation of a reproducible environment.

Interaction 3: FastF1 Telemetry Visualization

1. Context: Visualizing telemetry data (Lap-Time Distribution and Variance) to compare drivers Nico Hülkenberg (HUL) and Max Verstappen (VER).

2. Prompt(s): "Create a plot between the drivers 'HUL' and 'Ver' with the distribution of 'LapTimeSec' and the Variance"

3. Relevant Output: Python code using matplotlib and seaborn to generate a distribution plot and a variance subplot for the two drivers.

4. Validation: Ran the code in the Jupyter Notebook and checked if the visualizations correctly reflected the FastF1 telemetry DataFrame loaded in memory without throwing dimensional errors.

5. Adaptations: I adjusted the alpha (transparency) parameters, changed the plot colors to better match the visual style, and modified the overall figure size.

6. Final Decision: Partially used (Modified). The base logic for the subplots was helpful, but I needed to tweak the visual parameters manually for the final output.

Interaction 4: Jolpica API JSON Extraction

1. Context: Querying the Jolpica API for the 2024 driver standings and safely extracting nested data to meet the rubric's printing requirements.

2. Prompt(s): "Import the Jolpica API in JSON format, printing the HTTP status, number of records, and print the first 3 driver entries. If there is no driver, replace with 'N/A', create a function for this"

3. Relevant Output: Python code implementing a requests.get call with defensive programming (.get('key', 'N/A')) to avoid KeyError exceptions, wrapped in a function.

4. Validation: Executed the API call and manually printed the record_set[0].keys() and the raw JSON structure to verify that the keys used in the AI's code (givenName, points) actually existed in the hierarchy.

5. Adaptations: Removed the function wrapper to keep the data variables in the global notebook scope. I also explicitly added the .json extension to the endpoint URL to guarantee the correct response format.

6. Final Decision: Partially used (Modified). The AI's defensive extraction logic was kept, but the architecture was flattened to better fit a sequential Jupyter Notebook execution.

Interaction 4: Creating a ste-step documentation guide

1. Context: Deliver a document and step by step plan to install and run the project for a new user with no knloedge

2. Prompt(s): "In based in the Project and running celds, Create a 'README.md' document where in based in my operating system windows and the file requirements.txt , include the exact shell comands to download the repository and run the two notebooks, my github repository: 'https://github.com/marguerr04/iit414w-lab00-marguerr04' "

3. Relevant Output: A stet-by-step document for preparation and installation

4. Validation: Review the preparation, compare with the information of my repositoryl, also uninstall my virtual enviroment and follow the guide to check for errors

5. Adaptations: I added some information and tipping corrections in the README.md, correct names, and a little comments to give more clarify.

6. Final Decision: Partially used (Modified) , The AI give me a guide to setup and run my enviroment, fixin the possible errors, I read the outpout and modify adding more information or details.