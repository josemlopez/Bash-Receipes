# Bash-Receipes
Bash Receipes


Using grep colors, let's say we want to color some words in a log file:

tail -f planner.log  | egrep-red "(A new Event has arrived|)" | egrep-green "(Managing action success|)" | egrep-cyan "(The campaign has reach it's Initial time|)" |  egrep-redBack "(Traceback|Error|ERROR|)"

Let's say we want color some words in a log file and we want to remove some other words:

cat nohup.out | egrep --line-buffered -v "(Error in JSON sent like Event|New Event. Not validated yet)" | egrep-red "(A new Event has arrived|)" | egrep-green "(Managing action success|)" | egrep-cyan "(The campaign has reach it's Initial time|)" |  egrep-redBack "(Traceback|Error|ERROR)"



