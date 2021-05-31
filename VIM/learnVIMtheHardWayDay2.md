


2021-03-31

## BASIC MAPPING 

- Vimscript's most powerful feature is its ability to fine grain control of mapping the keyboard 
- We will begin by mapping in normal mode
                - :map - x (this maps the hyphen to the *x* which is the Vim command to delete
                    under the cursor (but not insert)
                    - :map - dd (this maps the command *dd* which deletes a line to the hyphen) 

## SPECIAL CHARACTERS 

- You can use <keyname> to tell Vim about special keys 
                - :map <space> viw
                - :map <c-d> dd *note here <c-d> means CTRL + d* 
                - On my own I tried the following:

                            *:map <space> vw* which doesn't go into insert mode after visual selection
        
                            *:map <space> v0* which selects from the last character in a line to the beginning of the line.



## EXERCISES 

-[x]  *Map the - key to "delete the current line, then paste it below the one we're on now". This will let
you move lines downward in your file with one keystroke*

-[x] *Add that mapping command to your ~/.vimrc file so you can use it any time you start Vim*.

-[] *Figure out how to map the _ key to move the line up instead of down.*

-[] *Add that mapping to your ~/.vimrc file too.*

-[x] *Try to guess how you might remove a mapping and reset a key to its normal function.*







'This is basic text for editing' 







