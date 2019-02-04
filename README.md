# motd_ascii_art
# Basic guide to color the ASCII art
# Basic coloring with "tput xterm"

# Set text color "foreground" with setaf
echo "$(tput -T xterm setaf 'color_number')"
echo "$(tput -T xterm setaf 2)"
# colors the text red

# Set background color with setab
echo "$(tput -T xterm setab 'color_number')"
echo "$(tput -T xterm setab 6)" 
# colors the background cyan

# The basic 8 color options
        0 = black
        1 = red
        2 = green
        3 = yellow
        4 = blue
        5 = magenta
        6 = cyan
        7 = white
#-----------------------------------------------------
# Using PS1 shell for bold and underlined ascii

# PS1 to underline ASCII chars 
printf "\e[4m"

# PS1 for Bold text / ASCII 
printf "\e[1m"

# For both Bold and underlined option on one line
printf "\e[1m\e[4m"

#-----------------------------------------------------
# Example Linux bash script "recreate the cyan horse"
Add printf "\n" (newline) if needed

#!/bin/bash
printf "\e[1m\e[4m"
echo "$(tput -T xterm setaf 6)"
printf "\n"
cat /your/path/to/ascii_art.txt
printf "\n"
