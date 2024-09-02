Madgen is a free-to-use web tool.

## Start
To start using Madgen, click the "Start" button on the home page. This will direct you to the login page, where you can log in using your email (for testing purposes, it is recommended to use a temporary email from various providers available online) or use the guest login. Once logged in, you will be directed to the calculator dashboard. The first page of the dashboard is the input page, where you can input the SMILES.

### Smile Input
You can have three types of inputs:
<br>
1. **Elemental**: To input elemental SMILES, a periodic table will open, allowing you to select elements and click submit.
<br>2. **Compound SMILES**: To input SMILES of individual compounds, for example, Methane (CH4) would be entered as `[H]C([H])([H])[H]`. After each entry, press enter and then submit.
<br>3. **Upload Files**: You can upload CSV or XLSX files. Files should have a header column named "Smiles".

You can use any or all of these input methods based on your needs. Once you finish the input, click the **"Analyze"** button to process the SMILES.
If everything is correct, a green check mark will appear next to each input button. You can view your files by clicking the **"View Files"** button.

#### View File 
When you click the ***"View Files"*** button, a window with a list of files will appear. If you use the elemental and compound input methods, you will see files with names starting with elementsXXXXX or compoundsXXXXX. 
The compounds and elemental inputs are in these files. If you want to change any of these inputs, please click the "View" button next to the files, which opens the file in a new window with three columns: Smiles, SmilesError, and Formula. The SmilesError column contains incorrect entries. You can sort the SmilesError column to quickly find any incorrect SMILES. If there are any incorrect SMILES, please correct them by clicking on the Smiles column (not SmilesError), then enter the correct SMILES. After inputting the correct SMILES, press enter (don't miss to press enter) and then click the "Update" button to save the changes. Once you have updated the changes, please close the window and click the "Analyze" button again. If everything is correct, a green check mark will appear next to each input button, indicating that you are ready to proceed to the next section.
### Calculator Selection
In this page, which is the Calculator Selection page, you can select calculators: First Gen, Second Gen, or Both. You can also select the Externals, RDKit or PubChem. Please note that PubChem is very slow. Once you have selected the calculator, press "Calculate". You can monitor the progress of the calculation from the loading button next to each selection. If all calculations are finished, you will see a green check mark next to each selection.

### Download/View Files
After this, go to the next page to download the files. You can download all files by clicking the "Download All Files" button or you can view the files by clicking the "Show Files" button. There is an "Export" button on the top right which can be used to download each file. If you download all files, you will get a .zip file with folders named elements, compounds, and uploads, which contain the descriptors from elements, compounds, and uploads.

To get an explanation of each column, refer to the section "Descriptor Data". If you are interested in a step-by-step guide, go to the section "Step-by-Step Guide".