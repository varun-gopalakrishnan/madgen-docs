
### Step 1: Login
- You can use either guest login or login with your email ID. In this version 0.1.0, we suggest using guest login or logging in with a temporary email. For this, you can use temporary mail services.

### Step 2: Smile Input
You can input SMILES in three forms:
  - **Elemental**: To input elemental SMILES, a periodic table will open, allowing you to select elements and click submit.
  - **Compound SMILES**: To input SMILES of individual compounds, for example, Methane (CH4) would be entered as `[H]C([H])([H])[H]`. After each entry, press enter and then submit.
  - **Upload Files**: You can upload CSV or XLSX files. Files should have a header column named "Smiles".

### Step 3: Analyze
After inputting your data, click "Analyze" to process the files. If everything is correct, a green check mark will appear next to each button.

### Step 4: Fix Errors
If there are any errors:
- Click "View Files" to open the file and check for entries in the "SmilesError" column.
- If there are entries in the "SmilesError," there is an issue with those SMILES. Correct the SMILES by clicking in the "Smiles" cell (not in "SmilesError") and editing the SMILES. Press "Update Smiles."
- After closing the dialog, press "Analyze" again. If everything is correct, a tick will appear next to the corresponding input.


### Step 5: Descriptor Selection
- Select either "First Gen," "Second Gen," or "Both."
- Click "Externals" if you want to generate descriptors, or choose "RDKit" or "PubChem" (note: these options may be very slow).

### Step 6: Click Calculate

### Step 7: Download Files
- Click "Download All Files" to download your files, or "Show Files" to view the files.

## Reminder
This is a beta version. Please don't input large files as this is deployed on a resource-limited platform.



