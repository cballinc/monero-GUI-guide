## Guide for the Monero GUI wallet

This repository contains the guide for the [Monero GUI Wallet](https://github.com/monero-project/monero-gui/releases).
This document is meant to be updated continuously and **a new major release will be available whenever Monero publishes a new version of the GUI**.
&nbsp;

The guide is composed by several different markdown files (see the chaper 'structure'). For simplicity, we have an easy-to-consult version:
&nbsp;

**[monero-GUI-guide.md](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/monero-GUI-guide.md)**    
*(This version will be replaced soon with an HTML page and a lot of cool stuff.)*

### Table Of Contents

-   **Preface**
    -   Translations
    -   Windows Preparation
    -   Shortcuts
-   **Choose a Language**
-   **Create a Wallet**
    -   Create new wallet
        -   Add a password
        -   Daemon settings
        -   Run a full node
    -   Restore wallet from keys or mnemonic seed
        -   Restoring from seed
        -   Restoring from keys
    -   Open a wallet from file
    -   Create new wallet from hardware
        -   Create the wallet
-   **Send Monero**
    -   Address Book
-   **Receive Monero**
-   **Advanced Features**
    -   Solo mining
    -   Prove - Check
        -   Prove Transaction
        -   Check Transaction
    -   Shared RingDB
    -   Sign - verify
        -   Sign
        -   Verify
-   **Settings**
    -   Wallet
    -   Local Node
    -   Remote Node
    -   Log
    -   Info
    -   Seed and keys
-   **Binaries Verification**
-   **About remote nodes**
    -   Bootstrap nodes
-   **Common issues and solutions**


## Structure and guidelines for contributors
The original guide can be found in the [en](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en) folder. It's divided in 9 main chapters:

**Chapter**|**Content**
---|--- 
00 | [Preface](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch00.md)
01 | [Choose a Language](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch01.md)
02 | [Create a Wallet](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch02.md)
03 | [Send Monero](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch03.md)
04 | [Receive Monero](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch04.md)
05 | [Advanced Features](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch05.md)
06 | [Settings](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch06.md)
07 | [Binaries Verification](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch07.md)
08 | [About remote nodes](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch08.md)
09 | [Common issues and solutions](https://github.com/monero-ecosystem/monero-GUI-guide/blob/master/en/ch09.md)

These single chapters can be built in a single file in 3 different formats: **HTML**, **PDF** and **EPUB**.    
To do so we use pandoc. If you wish to **build the guide by yourself**, you can do it following these steps (on Linux):

1. Download Pandoc and all necessary dependencies:
```
sudo apt install pandoc
sudo apt install texlive-full
```

2. From the source of the repository run:
```
make [format][-language]
```
For example, if you wish to build only the spanish version in PDF format, you should run `make pdf-es`.    
If you want all languages in a single format: `make epub`- This will give you the epub version in all languages.    
If you want to build all formats for all available languages: `make all` - This will build the guide in PDF, HTML and EPUB in all available languages.

### Contribute!
Improvements are always welcome. Feel free to propose a change using the issue tracker or opening a pull request.    
If you wish to contribute, please **do not** edit the file *monero-GUI-guide.md*. That's just temporary and it gets built manually. Work ONLY on the *.md* files inside the 'en' folder. Every pull request with changes to *monero-GUI-guide.md* will be rejected.

## Translations
Before adding a translation, please keep in mind the general guidelines for Monero translators, which are:

- **Avoid** the use of **gender specific** terminology.
- If available, use the **glossary** for your language. This will help to keep translations consistent across different works. You can find all glossaries [here](https://github.com/monero-ecosystem/monero-translations/tree/master/terminology-guides).
- Read the guide '[Translation tips for Monero translators](https://github.com/monero-ecosystem/monero-translations/blob/master/translation-tips.md)'. **It cointains all the informations you need** to submit a perfect translation.
- If a string contains numbers, just keep them as they are.

### Steps
Adding a translation is very easy:

1. Copy the *en* folder with all its content (including the 'makefile') and rename the new folder with the codename of your language (for example */it* for Italian).
2. Translate all the text you find, except for code and html.
3. Edit the string `LANGUAGES =` in the main makefile, after 'en' (or the previous added language) add the name of the folder which contains your translations.
4. Push the changes to your local branch and open a pull request.

### Support
If you need **help/support**, open an issue on this repository or contact ErCiccione. You can do so:
  
+ On the **live support chat of the localization workgroup**: `#monero-translations` (on IRC/Freenode, MatterMost, riot/matrix)
+ By **email**: translate[at]getmonero[dot]org
+ On **reddit**: just PM /u/erciccione

