I. PREPARE A CMS SITE AND IMPORT BACPAC FILE

1. Alloy CMS template is installed the latest headform API
Refer to the doc Installation Optimizely Forms Service.docx in https://episerver99.sharepoint.com/sites/HanoiQA/Delade%20dokument/Forms/AllItems.aspx?id=%2Fsites%2FHanoiQA%2FDelade%20dokument%2FAddons%2FADD%2DON%20DOCS%2F%5FInternal%20Add%2Dons%2F%5FnetCore%2F%2Enet6%2F1%2EForms%2FForm%20Headless%2FAPI&viewid=a40949c7%2Df5ab%2D4963%2D8360%2Da059c1ab3cad
for example the latest headless form package now <PackageReference Include="Optimizely.Cms.Forms.Service" Version="1.0.0-pre-545" />

2. import epicms.bacpac file into the database of the site

3. Open the site to be ready for running newman report below

II. CREATE REPORT BY NEWMAN

1.Create  a folder, for example d:\report

2. run cmd command and install newman
npm install -g newman

3. Copy data foler and file .json (FormHeadless v1.1.postman_collection.json) to d:\report

4. Run the Collection with Newman

to performance regression testing, you must to run folder regression as command below:

newman run "FormHeadless v1.1.postman_collection.json" --folder "Regression" -r htmlextra

5. View the result in newman folder
