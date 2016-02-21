# Bash-Receipes
Bash Receipes


Using grep colors, let's say we want to color some words in a log file:

```
tail -f planner.log  | egrep-red "(A new Event has arrived|)" | egrep-green "(Managing action success|)" | egrep-cyan "(The campaign has reach it's Initial time|)" |  egrep-redBack "(Traceback|Error|ERROR|)"
```

Let's say we want color some words in a log file and we want to remove some other words:

```
cat nohup.out | egrep --line-buffered -v "(Error in JSON sent like Event|New Event. Not validated yet)" | egrep-red "(A new Event has arrived|)" | egrep-green "(Managing action success|)" | egrep-cyan "(The campaign has reach it's Initial time|)" |  egrep-redBack "(Traceback|Error|ERROR)"
```



```
alias egrep-cyan="GREP_COLOR='1;36' egrep --line-buffered --color=always"
alias egrep-green="GREP_COLOR='1;32' egrep --line-buffered --color=always"
alias egrep-red="GREP_COLOR='1;31' egrep --line-buffered --color=always"
alias egrep-brow="GREP_COLOR='1;38' egrep --line-buffered --color=always"
alias egrep-yellow="GREP_COLOR='00;38;5;226' egrep --line-buffered --color=always"
alias egrep-purple="GREP_COLOR='1;35' egrep --line-buffered --color=always"
alias egrep-blue="GREP_COLOR='1;34' egrep --line-buffered --color=always"
alias egrep-redBack="GREP_COLOR='30;48;5;196' egrep --line-buffered --color=always"
```

