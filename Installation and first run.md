# Installation and first run

## Requirements
- Mongo DB Community Server 5.0.x

## Installation
1. Set up your MongoDB Community Server with access control disabled, commenting the following lines on file ```mongod.cfg``` in your Mongo Server directory (it should be like this by default):
```
#security:
#    authorization: enabled
```
2. Install and run Localization Tester Helper. You will be prompted with a login screen:
      - Press 'Settings', insert your mongo server address ('mongodb://localhost:27017', for example)
      - If the Mongodb server is empty and access control is disabled, a skeleton for the tool and a super user 'LocAdmin' account will be created.
3. Exit Localization Tester Helper and enable Mongo access control, un-commenting the previous lines on ```mongod.cfg``` file:
```
security:
    authorization: enabled
```
4. Restart Mongo DB Server.
5. Run Localization Tester Helper and login with the super user 'LocAdmin' (First time password is 'LocAdmin', you will be asked for a new password on login).
6. Create manager/testers accounts as needed. Please note that 'LocAdmin' account is not meant for regular use, and you should instead create manager accounts for normal use.

## Importing files

Using a manager account, and aAfter creating a project, get to the project management window (Admin->Project management) and click 'Import'. Select the project to import to, the row where the column headers are located and confirm.

Xlsx and xlsb files are supported, but is reccommended to stick to xlsx, as xlsb files are converted into xlsx anyway automatically and Excel needs to be installed in order to make the conversion. Regardless of the format, you will get the same format that you imported while exporting.
While importing a set of files, these files need to have the same column headers. The only exception is having a column header with a format like 'French (Translation)', 'Spanish (Translation)'..., while the rest of the columns headers remain identical.

If the files are compatible, you'll be prompted with a language selection for each of the files. If the languages in the filenames follow ISO 639-1 ('en-US' code, for example), or in 'Language (Country)' format, as in 'Spanish (Mexico)', languages should be automatically filled in the dropdown. If not, fill them and continue.

Now you'll be asked to select the tool fields for each column. All fields but 'Loc info' are mandatory. Column order can change between exports/files, so if you have a set of files with a column order and another set of files with a different order in the same project, just import them separately.
If your file has data validation columns, with user dropdown multiple selection ('status' column, for example) you'll be asked to select one of these columns, and its content and dropdown selector will appear in the 'Loc info' column in the main window.

Once the column order is selected, files will be imported and the localization testing proccess can start. Each new import will be named with the date and time of import, and will be selectable in right corner of the main window, with the last import being selected by default.

## Importing glossaries/termbases

For now, the only supported format for importing termbases is xlsx. The ideal way of importing termbases is with a single file that contains a 'term' column in the source language and several columns for each language. There is support for an all languages 'notes' column and each language can have an altenative term. Glossaries can also be imported with a file for each language, just make sure that you don't select other languages while importing glossaries. Glossary importing always replaces the old glossary with the new one, so when you update a language with an existing glossary, the whole old glossary will get replaced with the new one.
As of now, the terms will be shown in the change window (double clicking in the 'testing changes' column to insert a change) when there are glossary terms in the selected cell/row.

## Exporting files

Exporting is very straight forward. Once you are ready to export a batch, select 'Export files' from the project admin window and you will be prompted with which project and which imported batch (usually the latest) you want to export. The result of the export is a file identical to the one you imported but with the testing changes/comments/validation columns filled. If you imported a xlsb file, you also get the xlsx file, in case anything happened in the coversion proccess, but these files should have identical content.
