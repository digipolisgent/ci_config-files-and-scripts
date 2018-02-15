# Digipolis CI config files and scripts

This repository contains config files and scripts used for a CI workflow at Digipolis Gent. At this moment, this is mainly to steer Codeclimate and Travis.

## Structure

There is a hierarchical folder structure that gives more specific config files in deeper folders. So you start in the most specific applicable folder and work your way up to use the config files.

## Extend

### .eslintrc

It is possible to extend the config files. In order to do so:
- Edit .codeclimate.yml and change the fetch path for .eslintrc to ".digipolisgent/.eslintrc"
- Created your own ".eslintrc" which looks like:
```json
    { 
      "extends": ".digipolisgent/.eslintrc", 
      "root": true, 
      "globals": { 
        "Drupal": true, 
        "drupalSettings": true, 
        "jQuery": true, 
        "ol": true 
      } 
    }
```
- Update .gitignore file: change ".eslinrc" to ".digipolisgent/.eslintrc"
