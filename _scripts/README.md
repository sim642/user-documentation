## Script overview

The Script has following commands available (each can be shown when called with the help parameter `-h` on any of the positional parameters)
- `$ python _scrtips/automate.py status [-e|--extended] [-m --markdown]` 
  - prints the current status to the console
  - `[-e|--extended]` prints the relevant pages (also applies to the markdown mode)
  - `[-m --markdown]` write the status int the markdown syntax and opens the file
  

- `$ python _scrtips/automate.py update [-e|--extended]`
  - updates all the redirecting pages and the index file of each language as well as the inlcude pages
  - `[-e|--extended]` prints the relevant pages
    
  
- `$ python _scrtips/automate.py clean [-e|--extended]`
  - removes all the generated pages, the help site may not work afterwards
  - `[-e|--extended]` prints the deleted pages
  
  
- `$ python _scrtips/automate.py removeHelpSuffix [-e|--extended]`
  - removes from all help pages the `Help` suffix and creates redirects for them, this gets also called on each `update`
  - `[-e|--extended]` prints the renamed pages


## Add a new language

Example: Italian (it)

1. Create `it` folder
2. Create `_scripts/localization/it.json` (copy `en.json` and delete/translate the values)
3. Run `_scripts/automate.py update`
4. Add the Italian index to the main index if some of the pages are translated into Italian

## Installatation Notes

### Windows

1. [Install Chocolatey](https://chocolatey.org/install)
2. `choco install python2`
3. Switch back to normal command prompt
4. `c:\tools\python2\Scripts\pip install python-frontmatter`