# DAY 1 


*Wed 31 Mar 2021 02:53:36 AM +0530*



## Echoing Messages 

- Type >echo in command-line mode 
- Type >echom in command-line mode
- Documentation from :h :echo 
            - :ec[ho] {expre} echoes expressions with a space in between
            - Uses "/n" to start a new line 
            - Uses "/r" to move the cursor to the first column
- Documentation from :h :echom
-           - Like echo (above) it echoes an expression
-           - Unlike echo (above), it echoes the respective expression as a *true message and
              stores it in message history*

              > *'When you're writing more complicated Vimscript later in this book you may find yourself wanting
to "print some output" to help you debug problems. Plain old :echo will print output, but it will
OFTEN disappear by the time your script is done. Using :echom will save the output and let you run
:messages to view it later.'* 


## Setting Options 

- Vim has many options that changes that way it behaves
- *:set number* and *:set no number* toggle line numbers on and off
- Notice these are *boolean* options
- Because these are boolean operators you can set these options to do the opposite of what they
    are asked. For instance *:set nonumber!* will toggle line numbers, while *:set number!* will
    toggle line numbers off 
- Adding *!* or *bang!* to boolean options toggle it to the opposite of what the non-bang variant
    will do 
- Checking options:
-   - You can ask Vim what an option is currently set to by using *?* 
-   - Run the following: 
-       - *set number*
        - *set number?*
        - *set nonumber
        - *set nonumber?*
        - Notice how the first *:set number?* displayed the number while the second displayed no
            number


 ## Options with Values  

- Some options take avalue instead of just being on or off. 
- Run the following commands and watch what happens after each:
        - *set number*
        - *set numberwidth=10*
        - *set numberwidth=4*
        - *set numberwidth?* [Notice how the ? alters the command to echo the value of
            *numberwidth* that has been set at the time]
        - The addition of *?* is available for options when you need to change or check what they
            are set at currently. For example, check the following commands out:
                    - *:set wrap?*
                    - *:set shiftround?*
                    - * set matchtime* 


## Setting Multiple Options at Once 

- You can specify more that option at a time in the *:set* 
        - *:set numberwidth=2*
        - *:set nonumber*
        - *:set number numberwidth=6*



> ### Exercises 
> Read :help 'number' (notice the quotes).
>
>Read :help relativenumber.
>
>Read :help numberwidth.
>
>Read :help wrap.
>
>Read :help shiftround.
>
>Read :help matchtime.
> 
>Add some lines that would be useful for you to your .vimrc file 

    **'number'** **'nu'**  *Boolean	(default off)*
			
	Print the line number in front of each line.  When the 'n' option is
	excluded from 'cpoptions' a wrapped line will not use the column of
	line numbers (this is the default when 'compatible' isn't set).
	The 'numberwidth' option can be used to set the room used for the line
	number.
	When a long, wrapped line doesn't start with the first character, '-'
	characters are put before the number.
	See |hl-LineNr|  and |hl-CursorLineNr| for the highlighting used for
	the number.
	
    **number_relativenumber**
