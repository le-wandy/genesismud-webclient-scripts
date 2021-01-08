DESCRIPTION:
  THESE SCRIPTS, WHEN USED AS PROVIDED, ARE KNIGHTS GUILD SPECIFIC.

  These scripts allow automatically rescuing specific people. The names of
  specific people are saved in the player's userdata through the alias command.
  It can be quickly turned on and off through the command line.

  THIS IS ONLY INTENDED TO WORK FOR PLAYERS WITH INTRODUCED NAMES.

PARTS:
  1 alias
    "knights-rescue/aliases/autoresc.txt"
  1 trigger
    "knights-rescue/triggers/autoresc -- rescue.txt"

ALIAS COMMAND NAMING STRICTNESS:
  Not strict

SYNTAX:
  This assumes default alias names.

  autorescue add (name)
  -- Adds a name in the player's userdata as an autorescue target.
  -- (name) -> another player's introduced name

  autorescue remove (name)
  -- Removes a name from the player's userdata as an autorescue target.
  -- (name) -> another player's introduced name

  autorescue list
  -- Prints all the remembered autorescue targets into the main screen.

  autorescue clear
  -- Clears the list of remembered autorescue targets.

SETUP:
  Alias: autoresc.txt
    Recommended command: autorescue
    Script type: Javascript
    Instructions:
      Simply copy over the contents of the file into the code section.

  Trigger: autoresc -- rescue.txt
    Recommended name: autoresc -- rescue.txt
    Trigger pattern: ^(.*) attacks (.*).
    Trigger type: Regexp
    Case sensitive: Does not matter
    Script type: Javascript
    Instructions:
      Simply copy over the contents of the file into the code section.
