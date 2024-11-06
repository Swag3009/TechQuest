## Emacs Commands
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-x C-c**                         | End Emacs session                                                                          |
| **C-g**                             | Quit partially entered command. *(Stops unresponsive commands)*                            |
| **C-x k**                           | Kill Buffer                                                                                |
| **C-x d**                           | Open directory                                                                             |
| **C-x d +**                         | Create new directory                                                                       |

### Move Commands
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-v**                             | Move forward one screenful                                                                 |
| **M-v**                             | Move backward one screenful                                                                |
| **C-l**                             | Move text around the cursor to the center of the screen                                     |
| **C-p**                             | Move to previous line                                                                      |
| **C-n**                             | Move to next line                                                                          |
| **C-f**                             | Move forward by character                                                                  |
| **C-b**                             | Move backward by character                                                                 |
| **M-f**                             | Move forward by word                                                                       |
| **M-b**                             | Move backward by word                                                                      |
| **C-a**                             | Move to the beginning of the line                                                          |
| **C-e**                             | Move to the end of the line                                                                |
| **M-a**                             | Move to the beginning of the sentence                                                      |
| **M-e**                             | Move to the end of the sentence                                                            |
| **M-Shift-<**                       | Move to the beginning of the whole text                                                    |
| **M-Shift->**                       | Move to the end of the whole text                                                          |
| **C-t**                         | Line swapping                                                                              |
| **M-t**                         | Line swapping                                                                              |
| **C-u *digits* *command***           | Repeat command with numeric argument                                                       |
| **C-u *line number* M-g M-g**       | Jump to the line number                                                                    |
| **M-g M-g *number***                | Go to line                                                                                 |

### Basic Operations
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-d**                             | Delete the next character after the cursor                                                 |
| **M-d**                             | Delete the next word after the cursor                                                      |
| **M-(DEL)**                         | Kill the word immediately before the cursor                                                |
| **C-k**                             | Kill from the cursor position to the end of the line                                       |
| **M-k**                             | Kill to the end of the current sentence                                                    |
| **C-(SPC)**                         | Highlight selected space                                                                   |
| **C-w**                             | Kill all the text between selected positions                                               |
| **M-w**                             | Copy                                                                                       |
| **C-y**                             | Yank (paste)                                                                               |
| **C-/**, **C-_**, **C-x u**          | Undo                                                                                       |
| **C-x C-f**                         | Find file                                                                                  |
| **C-x C-s**                         | Save the file                                                                              |
| **C-x C-b**                         | List of buffers                                                                            |
| **C-x b *buffer's name***            | Switch to a buffer                                                                         |
| **C-x s**                           | Save some buffers                                                                          |
| **C-x**                             | Exit Emacs temporarily                                                                     |
| **C-h m**                           | View documentation on current major mode                                                   |
| **M-x auto-fill-mode**              | Turn on/off Auto Fill mode                                                                 |
| **M-q**                             | Refill paragraph (with cursor inside the paragraph)                                        |
| **C-s**                             | Forward search                                                                             |
| **C-r**                             | Reverse search                                                                             |
| **C-t**                             | Switch two letters                                                                         |
| **M-t**                             | Switch two words                                                                           |
| **(ESC) (ESC) (ESC)**               | General purpose "get out" command (to exit recursive editing, extra windows, minibuffer)    |

### Help
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-h**                             | Help                                                                                       |
| **C-h c *command***                 | Brief description of a command                                                             |
| **C-h k *command***                 | Detailed information about a command                                                       |
| **C-h f *function_name***           | Describe function                                                                          |
| **C-h v *variable_name***           | Documentation of variable                                                                  |
| **C-h a *keyword***                 | Display all commands that contain the keyword                                              |
| **C-h i**                           | Read included manuals                                                                      |
| **C-h P**                           | Describe package                                                                           |
| **C-h m**                           | Help about specific module                                                                 |

### Windows
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-x 1**                           | One window                                                                                 |
| **C-x 2**                           | Split screen into two windows                                                              |
| **C-M-v**                           | Scroll bottom window                                                                       |
| **C-x o**                           | Switch between windows                                                                     |
| **C-x 4 C-f *file_name***           | Open file in bottom window                                                                 |
| **C-x 5 2**                         | Open a new frame                                                                           |
| **C-x 5 f**                         | Load a new file in a new frame                                                             |
| **C-x 5 b**                         | Open an existing buffer in a new frame                                                     |
| **C-x 5 0**                         | Remove the selected frame                                                                  |

### Buffers
| **Command**                         | **Description**                                                                            |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| **C-x b *buffer***                  | Select or create a buffer named *buffer*                                                   |
| **C-x 4 b *buffer***                | Select buffer in another window                                                            |
| **C-x 5 b *buffer***                | Select buffer in a separate frame                                                          |
| **C-x LEFT**                        | Select previous buffer in buffer list                                                      |
| **C-x RIGHT**                       | Select the next buffer in the buffer list                                                  |
| **C-x b**                           | Switch to buffer                                                                           |
| **C-x 4 m**                         | Check the message buffer                                                                   |
