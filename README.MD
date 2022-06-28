# Localization Tester Helper

Localization Tester Helper is a localization tool that acts as a proxy between the developer/client supplied excel/tabulated files and the localization testing department.
It streamlines the localization work in the testing side by automating a number of common tasks while providing a full set of tools for the testers and the managers.

- [General info and features](https://github.com/NaifeSoft/localization-tester-helper-releases#current-features)
- [Installation and first run](https://github.com/Potajito/localization-tester-helper-test/blob/main/Installation%20and%20first%20run.md)
- [Planned features](https://github.com/NaifeSoft/localization-tester-helper-releases/tree/main#planned-features)
- [Download releases]([https://github.com/NaifeSoft/localization-tester-helper-releases#current-features](https://github.com/NaifeSoft/localization-tester-helper-releases/releases))


### Current features
- [x] Fast searching even with huge datasets.
- [x] Inmediate as-you-type filtering.
- [x] Support for advanced search and filtering (begins with, ends with...) and plain regex.
- [x] Transparent solution. An Excel file comes in, an excel file comes out, so you can still use your pre and post proccessing tools as usual.
- [x] Support for split language files, that is, even if the same language is split in several files (OST, Interface...), importing, exporting and actual file work is transparent for the user. (As long as files share the same column structure!)
- [x] Spellchecker, with support for downloading more languages inside the app.
- [x] Full Unicode and right to left writting support.
- [x] Xlsx and xlsb support (xlsb needs Excel to be installed).
- [x] Data validation support for user selectable dropdowns, aka 'status' columns in the same view as the strings, one click away in order to minimize clutter.
- [x] Automatic filling of type of change, date and username when making a change.
- [x] Easy copy and pasting of previously validated changes.
- [x] Mass find and replace feature with preview of changes before commiting. Automatic comment adding while mass replacing.
- [x] Complete user system with manager roles, testing roles and per-project permissions granularity.
- [x] Change history per cell, with user, comment and date info. Past changes are also a click away, even in newly imported files.
- [x] Theming. System theme, dark theme and light theme.
- [x] Show context of strings. Instead of just showing matches, the results include strings that are 'near' the actual results (and differentiate them), thus giving more context on the strings shown.
- [x] CAT Termbase importing/referencing while making a change. Multiple termbase import, so it's possible to import 


 ### Workflow

This is a proxy solution to avoid working directly with excel files, which is slow and prone to errors. This is transparent for the developer/client, as they send an excel file and get an excel file in the same format.
The workflow would go as:
1. Manager creates a project and imports files. It could be a single file for each language or multiple files per language, in case the project splits the files. (columns must coincide between languages)
2. Manager assings testers to the project.
3. Testers work on the current file as usual.
4. When a delivery needs to be done, the manager will export the files with a single command and get an excel file with the testing changes and comments.
5. When new files arrive, the manager just has to import these new files to restart the proccess.

## Current features explained

#### Streamlined import of files, with automatic parsing of language filenames, so no more scrolling looking for the right language. ISO 639-1 support, as in 'en-US' codes, or 'Language (Country)' format, as in 'Spanish (Mexico)'.

![importing_1](https://user-images.githubusercontent.com/39760810/172073540-e9547d05-d4b3-46ad-8fa6-630632737c88.gif)

Select your column order and you are good to go!

![column_selector](https://user-images.githubusercontent.com/39760810/172073669-51d3f8b3-8345-4adb-9825-52e1940f2ddb.jpg)

#### Fast and responsive search

https://user-images.githubusercontent.com/39760810/172073623-9c10d875-c480-4f99-8444-0743cb940267.mp4

Fast, database based search, even in huge projects. Advanced search options, filtering and regex.

#### Inmediate filtering as-you-type

https://user-images.githubusercontent.com/39760810/172073745-3054f71c-e92e-4bac-9c0a-8eb5ed821845.mp4

Advanced filtering as-you-type, with common cascading filters (begins with, ends with, contains...) and regex support for advanced users.

#### Controlled, user based, change system and spellchecker

https://user-images.githubusercontent.com/39760810/172073805-28c73b74-dd16-46fc-86d0-20b2607d44d1.mp4

Commit change system in order to avoid typos, non-changes and lack of comments. Users can submit changes one by one or copy and paste already validated changes. 
All in real time, so the whole team would see the change as it's made.
The system also supports cell coloring, which shows both in the app interface and in the final export.

#### Safe find and replace functionality, with result preview and bulk commenting

https://user-images.githubusercontent.com/39760810/172073774-9534ebcf-8dc6-491f-bdd9-0eb9e07b5b24.mp4

Preview the find and replace change before actually commiting it, fix any corner case in the spot and confirm the change inserting a bulk comment.

#### Historic database of testing changes

https://user-images.githubusercontent.com/39760810/172073970-1ea2cf98-2644-48fe-baaf-6e656006115d.mp4

Past changes are a click away, even when a new file as just been imported, it will show the cells that have seen changes in the past, so managers and testers know the full context and history easily.

#### Complete user system with full role management in a per-project basis, differentiating testers and managers.
Full user system with permissions for each projecta, all seamlessly integrated in the multilanguage workflow, allowing testers to look for reference at other languages strings easily.

#### Data validation with multiple user choice inside the actual interface

![2022-06-07_17-54](https://user-images.githubusercontent.com/39760810/172439443-f0f1af15-45ea-4316-a94a-c933f79d89a0.png)


## Planned features

- [ ] Statistics and data visualization. Number of changes per language, per tester, most changed strings...
- [ ] Tag system in editor. No more '\n' and <random tags> in the source that hamper reading and are easy to mess up. Instead a graphical tag should show, and could only be edited willingly.
- [ ] Character limit implementation. Warning when over character limit.
- [ ] Cross-checking for changes between languages. Detect when a change done in a language could be replicated in others.
 
  

