## Org Mode Commands

| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-t**                         | Cycle TODO state of the current item (TODO, DONE)                                          |
| **C-c ,**                           | Set tags for the current headline                                                          |
| **C-c C-c**                         | Set or change a property of the current item                                               |
| **C-c C-s**                         | Schedule a task                                                                            |
| **C-c C-d**                         | Set a deadline for a task                                                                  |
| **C-c C-l**                         | Insert or edit a hyperlink                                                                 |
| **C-c C-o**                         | Open a link                                                                                 |
| **C-c C-x C-i**                     | Clock in to start tracking time for the current task                                       |
| **C-c C-x C-o**                     | Clock out to stop tracking time for the current task                                       |
| **C-c C-x C-e**                     | Evaluate code block                                                                        |
| **C-c C-x C-r**                     | Refresh dynamic blocks                                                                     |
| **C-c C-x C-f**                     | Toggle the state of a footnote at point                                                    |
| **C-c C-x p**                       | Mark current subtree as archived                                                           |

### Movement and Structure
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-n**                         | Move to the next heading                                                                   |
| **C-c C-p**                         | Move to the previous heading                                                               |
| **C-c C-u**                         | Move up one level in the hierarchy                                                         |
| **M-LEFT**                          | Promote the current heading                                                                |
| **M-RIGHT**                         | Demote the current heading                                                                 |
| **M-UP**                            | Move the current heading or item up                                                        |
| **M-DOWN**                          | Move the current heading or item down                                                      |
| **C-c @**                           | Mark a subtree for export                                                                  |
| **C-c C-w**                         | Refile the current item to a different location                                            |

### Visibility
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **TAB**                             | Cycle visibility between folded, subtree, and entire document                              |
| **S-TAB**                           | Global visibility cycling                                                                  |
| **C-c C-r**                         | Reveal the current entry and its subtree                                                   |
| **C-c C-x b**                       | Toggle sparse tree highlighting                                                            |
| **C-c C-x v**                       | Toggle the visibility of inline images                                                     |

### Editing
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **M-RET**                           | Insert a new heading or list item                                                          |
| **M-S-RET**                         | Insert a new TODO item                                                                     |
| **C-c -**                           | Insert a horizontal line or list separator                                                 |
| **C-c ' (apostrophe)**              | Edit the source code block in its native major mode                                        |
| **C-c ^**                           | Sort entries or lists                                                                      |
| **C-c \***                          | Set a headline level to a specific value                                                   |
| **C-c C-q**                         | Set priority for the current item                                                          |

### Time and Scheduling
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c .**                           | Insert a timestamp                                                                         |
| **C-c C-d**                         | Set a deadline date                                                                        |
| **C-c C-s**                         | Schedule a task                                                                            |
| **C-c C-x C-t**                     | Insert a timestamp for a repeating task                                                    |
| **C-c C-x C-i**                     | Start tracking time (clock in)                                                             |
| **C-c C-x C-o**                     | Stop tracking time (clock out)                                                             |
| **C-c C-x C-r**                     | Show the clock report for the current buffer                                               |

### Exporting
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-e**                         | Open the export dispatcher                                                                 |
| **C-c C-e h**                       | Export as HTML                                                                             |
| **C-c C-e l**                       | Export as LaTeX                                                                            |
| **C-c C-e o**                       | Export as ODT (OpenDocument Text)                                                          |
| **C-c C-e t**                       | Export as a plain text file                                                                |
| **C-c C-e d**                       | Export as DocBook                                                                          |
| **C-c C-e i**                       | Export as iCalendar                                                                        |

### Checkbox Commands
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-c**                         | Toggle checkbox status                                                                     |
| **C-c -**                           | Insert a checkbox                                                                          |
| **M-S-RET**                         | Add a new checkbox                                                                         |

### Capture and Agenda
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c c**                           | Start a capture process to add new tasks or notes                                          |
| **C-c a**                           | Open the agenda view                                                                       |
| **C-c C-x C-a**                     | Archive the current entry                                                                  |
| **C-c C-x C-j**                     | Jump to a stored agenda location                                                           |
| **C-c C-x C-f**                     | Create a clocktable report                                                                 |

### Hyperlinks
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-l**                         | Insert or edit a hyperlink                                                                 |
| **C-c C-o**                         | Follow a hyperlink                                                                         |
| **C-c C-x o**                       | Open a URL-like link                                                                       |

### Tables
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c |**                           | Create a table                                                                             |
| **TAB**                             | Move to the next field in a table                                                          |
| **M-TAB**                           | Recalculate a formula                                                                      |
| **C-c C-x M-t**                     | Toggle automatic table realignment                                                         |
| **C-c C-c**                         | Recalculate all formulas in a table                                                        |
| **C-c ****                          | Sum the current column in a table                                                          |

### Code Blocks
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-v t**                       | Evaluate the current code block                                                            |
| **C-c C-v d**                       | Display the results of the current code block                                              |
| **C-c C-v c**                       | Execute code block                                                                         |
| **C-c C-v e**                       | Export code block results                                                                  |
| **C-c C-v i**                       | Insert a source code block                                                                 |

### Miscellaneous
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-c C-z**                         | Switch back to the previous buffer                                                         |
| **C-c C-x C-s**                     | Save the current buffer and clock report                                                   |
| **C-c C-x p**                       | Mark the current subtree as archived                                                       |
| **C-c C-x b**                       | Toggle sparse tree highlighting                                                            |
| **C-c C-x C-f**                     | Toggle inline footnotes                                                                    |
