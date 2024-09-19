### Home Page:
When you open the website, you will be directed to the home page, which has two options:

- **Tutorial**: This will direct you to this documentation page. (If you are seeing this page, you already know what that button does.)
- **Start**: This will direct you to the login page.

### Login
The typical login page allows you to log in with your email ID or as a guest.  
![Login Page](images/login.png)  
For now, we strongly recommend using guest login (**CONTINUE AS GUEST**) or logging in with a temporary email ID (you can use temporary mail services). We’d love to see how logging in with an email ID works, so if you want to join our experiment, you are free to do so.

!!! warning "Remember"
    **Please note that all files will be deleted 1 hour after login. If you are still using the site after 1 hour, please log out and log in again (currently, we have not implemented auto-logout).**

### Dashboard
Once you are logged in, you will be directed to the dashboard.  
![Dashboard](images/dashboard.png)  
The page is about **SMILES** input. Here we have three options:

- **Elemental**: To input elemental SMILES, a periodic table will open, allowing you to select elements and click submit (only elements are allowed at this stage).  
  ![Elemental](images/periodictable.png){:height="50%" width="50%" align="right" loading="lazy"}  
  The image on the right is the periodic table. You can select elements by clicking on them. After selecting the elements, click "Submit."

!!! info "Info"
    Currently, only elements can be selected (multiple elements are allowed), but formulas are not allowed. For example, if you select C and O, it will be considered as elemental Carbon and Oxygen, not as Carbon Monoxide.

- **Compound SMILES**: To input SMILES of individual compounds. For example, Methane (CH₄) would be entered as `[H]C([H])([H])[H]`. After each entry, press enter.  
  ![Compound](images/compoundsmiles.png){:height="50%" width="50%" align="left" loading="lazy"}  
  When an entry is recorded, you will see a green shade around the SMILES. In the image on the left, we entered three SMILES. After each SMILES entry, press enter and then input the next SMILES (one by one). When finished, click the submit button.

---
- **Upload Files**: You can upload CSV or XLSX files. Files should have a header column named "Smiles."  
  ![Upload](images/smiles_file.png){:height="20px" width="110px" align="right" loading="lazy"}  
  The image on the right shows a sample file. The header in row 1 should be exactly "Smiles."  
  ![Upload](images/uploads.png){:height="50%" width="50%" align="left" loading="lazy"}  
  Click "Choose File" to select a file from your computer. After selecting the file, click "Submit."

!!! tip "Multiple Inputs"
    In the above image, you can see that all three options are in black, meaning they are selected. You can use all three inputs at the same time.

___

!!! info "Info"
    You may see the info icon (:material-information-box-outline:). On mobile, tap it, and on a personal computer, hover over it to see additional tips or information, like this:
    ![info.png](images/infoicon.png)

### Analyze
After inputting your data, click "Analyze" to process the files. 
If everything is correct, a green checkmark (:octicons-checkbox-16:{.checkmark}) will appear next to each button.
If ,there is an error, an excalamation in red triangle (:fontawesome-solid-triangle-exclamation:{.error_exmtn}) will appear next to the button.

The main purpose of the analyse button is filter and correct the SMILES, this would be very helpful in files. After analysing you can view the files and correct inputs and it will discuss in next section

### Fix Errors (View Files)
If there are any errors or you want to change something,

- Click "View Files" to open the file which lead to a new window like this,
    ![View Files](images/viewfilelist.png){:height="50%" width="50%" align="center" loading="lazy"}
Here you can see the status is **Error** which means there is an error in some of the entries. 
---
- To inspect the file, please click view which opens the file in a new window.If there are entries in "SmilesError," there is an issue with those SMILES. Correct the SMILES by clicking in the "Smiles" cell (not in "SmilesError") and editing the SMILES. Press "Update Smiles."
  ![View File](images/smileserror.png){:height="50%" width="50%" align="right" loading="lazy"}  
 In the image on right side we see that "T" is not a valid SMILES, so only the row corresponding have an entry in **SmilesError** column all other entries are empty. Now we need to correct the T. 
For that we click on T (we are correcting this to say [Ti] ,Tiatanium) in **Smiles** column :material-arrow-right: Correct the Smile (to [Ti]) :material-arrow-right: Press enter (++enter++) :material-arrow-right: Click Update (:octicons-sync-16:{color:green}) button
---
 ![View File](images/smileserrorupdated.png){:height="50%" width="50%" align="left" loading="lazy"}  
  The image on left is after updation, you can see that the "T" is corrected to "[Ti]" and we get a notification that the entry is updated.
  
 For verification you can click Analyse again and check the status of the file. If there are no errors, you can proceed to the next step. If there are errors, you can correct them and re-analyse the file.

!!! info "Remember"
    Only edit the "Smiles" Column, not the "SmilesError" Column. SmilesError is to idenetify erroneus entries quickly. You can use <span style="display:inline-block; transform: rotate(90deg);">:octicons-arrow-switch-16:</span> to sort the column and find the erroneous entries quickly.
---
!!! tip "Tip"
    You can use the search bar to search for a specific entry in the file.
   
!!! info "Filenames"
    The filename starting with elements or compunds and ending with <some alphanumric> contains those entries from Elements and Compounds input.
### Descriptor Selection
- Select Generations or Externals
- Generations will intend to generate the basic descriptors like atomic number, valence number etc. More details on this descriptor can be found in [**Descriptor File**](descriptorfile.md) section
- Click "Externals" if you want to generate descriptors, or choose "RDKit" or "PubChem"

!!! info "Info"
    This section will update in future
- Click "Calculate" to generate the descriptors.

### Download Files
Click "Download All Files" to download your files (in zip format), or "Show Files" to view the files.
![Download Files](images/downloadfiles.png){:height="50%" width="50%" align="right" loading="lazy"}
  


---
## Reminder
This is a beta version. Please avoid uploading large files (it is better if you don't upload any files, we know this sounds not good and defeat the entire purpose, but please bear with us for this moment), as this is deployed on a resource-limited platform.
