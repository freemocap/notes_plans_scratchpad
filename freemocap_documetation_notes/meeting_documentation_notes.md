# Notes for FreeMoCap documentation

[![hackmd-github-sync-badge](https://hackmd.io/wY3Bb7iYQMemqIBXKzPGew/badge)](https://hackmd.io/wY3Bb7iYQMemqIBXKzPGew)

## 2022-08-05 
 in meeting - Jon, Trent, Kiley, Aaron
 
 - Discuss - 
     - Mechanisms of building docs
         - mkdocs
         - gh-pages
     - workflow
         - pull requests etc
         - 

Having images leads to problems because it makes the repo big 
- Options: 
    - no photos (which would be a bummer)...not actually an option
    - linked external site (how?)
    - separate repo for documentation
        - but then need to figure out how this operates with auto-generated stuff from `docstrings` etc


https://realpython.com/python-project-documentation-with-mkdocs/

Bottlenecks: 
 - need new codebase up to funcationality to start adding docstrings and whatnot
### basic content - 
 - follow `diataxis` format
     - https://diataxis.fr/
     - see also [diviio](https://documentation.divio.com/)
 - Tutorials
     - hand holdy intro stuff
 - How-to guides
     - more specific, drier instructions
     - trouble shooting guides
 - Reference
     - Python API (function, classes, etc,)
         - built via docstrings, etc
     - Glossary
         - terminology
     - FAQ?
 - Explanation
     - educational content
     - explaining deeper content, contexts, etc
     - understanding the deeper level of how thing work and how they might be used in practice
     - i.e. the kind of stuff I would teach a class about
 
### stuff that is kinda blocked
- Tutorial 
    - we *could* do a pre-alpha tutorial now
    - but I think I'd rather wait until Alpha
- Python API 
    - docstrings etc should come from 'alpha' codebase
### Stuff we can do right now
- FAQ
    - Comb through the server (esp in the #help-requests and #freemocap-discussion channels) and look for:
        - 'good' replies from:
            - Jon
            - Trent
            - Aaron
            - Philip
            - etc
        - basically anytime someone from our end offered a detailed explanation to a question
        - Create a list of questions before answering them. 
            - Here's Trents Draft 1 of an FAQ: https://github.com/freemocap/freemocap/wiki/FAQ
    - make a list somewhere with: 
        - a link to the discord comment
        - a few phrases about the content like "installation problems" or "how to choose a camera" etc
        - Sanity check answers with Jon, Aaron, Trent, etc. 
