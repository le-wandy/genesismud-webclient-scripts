DESCRIPTION:
  These scripts record every line that appears since activated, appending a
  time stamp based on your computer computer time.

  Stopping the script will start a download of the log file through the browser.

PARTS:
  1 alias
    "log-maker/aliases/log.txt"
  1 trigger
    "log-maker/triggers/log -- record lines.txt"

ALIAS COMMAND NAMING STRICTNESS:
  Not strict

SYNTAX:
  This assumes default alias names.

  log start
  -- Starts logging.

  log stop
  --  Stops logging and creates download for log text file.

SETUP:
  Alias: log.txt
    Recommended command: log
    Script type: Javascript
    Instructions:
      Simply copy over the contents of the file into the code section.

  Trigger: log -- record lines.txt
    Recommended name: log -- record lines
    Trigger pattern: (.*)
    Trigger type: Regexp
    Case sensitive: Does not matter
    Script type: Javascript
    Instructions:
      Simply copy over the contents of the file into the code section.
