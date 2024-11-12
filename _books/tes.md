st login: Mon Nov 11 15:51:13 on ttys000
/Users/jakob/.zprofile:8: bad pattern: ^[[D^[[B
jakob@MacBookAir ~ % task
zsh: command not found: task
jakob@MacBookAir ~ % task list
zsh: command not found: task
jakob@MacBookAir ~ % brew help
zsh: command not found: brew
jakob@MacBookAir ~ % brew install task
zsh: command not found: brew
jakob@MacBookAir ~ % /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
==> Checking for `sudo` access (which may request your password)...
Password:
==> This script will install:
/opt/homebrew/bin/brew
/opt/homebrew/share/doc/homebrew
/opt/homebrew/share/man/man1/brew.1
/opt/homebrew/share/zsh/site-functions/_brew
/opt/homebrew/etc/bash_completion.d/brew
/opt/homebrew

Press RETURN/ENTER to continue or any other key to abort:
==> /usr/bin/sudo /usr/sbin/chown -R jakob:admin /opt/homebrew
==> Downloading and installing Homebrew...
==> Updating Homebrew...
Warning: /opt/homebrew/bin is not in your PATH.
  Instructions on how to configure your shell for Homebrew
  can be found in the 'Next steps' section below.
==> Installation successful!

==> Homebrew has enabled anonymous aggregate formulae and cask analytics.
Read the analytics documentation (and how to opt-out) here:
  https://docs.brew.sh/Analytics
No analytics data has been sent yet (nor will any be during this install run).

==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations

==> Next steps:
- Run this command in your terminal to add Homebrew to your PATH:
    eval "$(/opt/homebrew/bin/brew shellenv)"
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh

jakob@MacBookAir ~ %     eval "$(/opt/homebrew/bin/brew shellenv)"

jakob@MacBookAir ~ % brew install task
Warning: task 3.1.0 is already installed and up-to-date.
To reinstall 3.1.0, run:
  brew reinstall task
jakob@MacBookAir ~ % task
No matches.
jakob@MacBookAir ~ % task list
No matches.
jakob@MacBookAir ~ % brew reinstall task
==> Downloading https://ghcr.io/v2/homebrew/core/task/manifests/3.1.0
jakob@MacBookAir ~ % task
No matches.
jakob@MacBookAir ~ % task
No matches.
jakob@MacBookAir ~ % data.location=~/.task
zsh: no such file or directory: data.location=~/.task
jakob@MacBookAir ~ % deinstall task
zsh: command not found: deinstall
jakob@MacBookAir ~ % 
jakob@MacBookAir ~ % task
No matches.
jakob@MacBookAir ~ % which task
/opt/homebrew/bin/task
jakob@MacBookAir ~ % brew install task
Warning: task 3.1.0 is already installed and up-to-date.
To reinstall 3.1.0, run:
  brew reinstall task
jakob@MacBookAir ~ % task
No matches.
jakob@MacBookAir ~ % task add Testaufgabe
Created task 1.
jakob@MacBookAir ~ % task list

ID Age  Description     Urg 
 1 3s   Testaufgabe        0

1 task
jakob@MacBookAir ~ % 
jakob@MacBookAir ~ % tast 1 done
zsh: command not found: tast
jakob@MacBookAir ~ % task 1 done
Completed task 1 'Testaufgabe'.
Completed 1 task.
jakob@MacBookAir ~ % task list
No matches.
jakob@MacBookAir ~ % task add GP2(Excel) due:tommorw                 
zsh: number expected
jakob@MacBookAir ~ % task add GP2 Ecel due:2024-10-12
Created task 1.
jakob@MacBookAir ~ % task list

ID Age  Due        Description  Urg 
 1 1min 2024-10-12 GP2 Ecel       12

1 task
jakob@MacBookAir ~ % tast due:2024-10-12 list
zsh: command not found: tast
jakob@MacBookAir ~ % task due:2024-10-12 list 

ID Age  Due        Description  Urg 
 1 1min 2024-10-12 GP2 Ecel       12

1 task
jakob@MacBookAir ~ % tast due:tomorow
zsh: command not found: tast
jakob@MacBookAir ~ % task due:tomorow
'tomorow' is not a valid date in the 'Y-M-D' format.
jakob@MacBookAir ~ % task add 1 projekt: Uni 
Created task 2.
jakob@MacBookAir ~ % task list

ID Age  Due        Description        Urg 
 1 3min 2024-10-12 GP2 Ecel             12
 2 7s              1 projekt: Uni        0

2 tasks
jakob@MacBookAir ~ % task add GP2 Ecel project: 'Uni'
Created task 3.
jakob@MacBookAir ~ % task

ID Age   Due   Description    Urg 
 1  4min -4w   GP2 Ecel         12
 2 56s         1 projekt: Uni    0
 3 12s         GP2 Ecel Uni      0

3 tasks
jakob@MacBookAir ~ % takk done 2,3
zsh: command not found: takk
jakob@MacBookAir ~ % task done 2,3 
This command will alter 2 tasks.
Completed task 2 '1 projekt: Uni'.
Completed task 3 'GP2 Ecel Uni'.
Completed 2 tasks.
You have more urgent tasks.
jakob@MacBookAir ~ % task add GP2 Ecel project:'Uni'
Created task 4.
The project 'Uni' has changed.  Project 'Uni' is 0% complete (1 task remaining).
jakob@MacBookAir ~ % task list uni
No matches.
jakob@MacBookAir ~ % task list

ID Age   Project Due        Description  Urg 
 1  5min         2024-10-12 GP2 Ecel       12
 2 17s   Uni                GP2 Ecel        1

2 tasks
jakob@MacBookAir ~ % task project

ID Age   Project Description Urg 
 2 38s   Uni     GP2 Ecel       1

1 task
jakob@MacBookAir ~ % task add GP2-Excel project:uni due:2024-11-12
Created task 3.
The project 'uni' has changed.  Project 'uni' is 0% complete (1 task remaining).
jakob@MacBookAir ~ % task due 2024-10-12 list
No matches.
jakob@MacBookAir ~ % task due: 2024-10-12 list 
No matches.
jakob@MacBookAir ~ % task list

ID Age   Project Due        Description   Urg 
 1  6min         2024-10-12 GP2 Ecel        12
 3 26s   uni     2024-11-12 GP2-Excel     9.65
 2  1min Uni                GP2 Ecel         1

3 tasks
jakob@MacBookAir ~ % task list due:204-10-12
Cannot subtract strings
jakob@MacBookAir ~ % task +WEEK list

ID Age  Project Due        Description   Urg 
 3 1min uni     2024-11-12 GP2-Excel     9.65

1 task
jakob@MacBookAir ~ % task done 3
Completed task 3 'GP2-Excel'.
Completed 1 task.
You have more urgent tasks.
The project 'uni' has changed.  Project 'uni' is 100% complete (0 of 1 tasks remaining).
jakob@MacBookAir ~ % task done 1,2
This command will alter 2 tasks.
Completed task 1 'GP2 Ecel'.
Completed task 2 'GP2 Ecel'.
Completed 2 tasks.
The project 'Uni' has changed.  Project 'Uni' is 100% complete (0 of 1 tasks remaining).
jakob@MacBookAir ~ % task list
No matches.
jakob@MacBookAir ~ % task add GP2-Excel proejec:uni due:2024-10-12
Created task 1.
jakob@MacBookAir ~ % task +WEEK list
No matches.
jakob@MacBookAir ~ % taskt list
zsh: command not found: taskt
jakob@MacBookAir ~ % task list

ID Age   Due        Description               Urg 
 1 24s   2024-10-12 GP2-Excel proejec:uni       12

1 task
jakob@MacBookAir ~ % tast +WEEK list
zsh: command not found: tast
jakob@MacBookAir ~ % task +WEEK list 
No matches.
jakob@MacBookAir ~ % task add Kochen due:TODAY
'TODAY' is not a valid date in the 'Y-M-D' format.
jakob@MacBookAir ~ % task add Kochen due:2024-10-11
Created task 2.
jakob@MacBookAir ~ % Task +DUETODAY list
No matches.
jakob@MacBookAir ~ % $ task +DUETODAY list
zsh: command not found: $
jakob@MacBookAir ~ % task +DUETODAY list 
No matches.
jakob@MacBookAir ~ % task list

ID Age   Due        Description               Urg 
 2 40s   2024-10-11 Kochen                      12
 1  2min 2024-10-12 GP2-Excel proejec:uni       12

2 tasks
jakob@MacBookAir ~ % task color

Basic colors
  black   red   blue   green   magenta   cyan   yellow   white 
  black   red   blue   green   magenta   cyan   yellow   white 

Effects
  red   bold red   underline on blue   on green   on bright green   inverse 

color0 - color15
  0 1 2 . . .
                  
                  
          . . . 15

Color cube rgb000 - rgb555 (also color16 - color231)
  0            1            2            3            4            5
  0 1 2 3 4 5  0 1 2 3 4 5  0 1 2 3 4 5  0 1 2 3 4 5  0 1 2 3 4 5  0 1 2 3 4 5
 0                                                                              
 1                                                                              
 2                                                                              
 3                                                                              
 4                                                                              
 5                                                                              

Gray ramp gray0 - gray23 (also color232 - color255)
  0 1 2 . . .                             . . . 23
                                                  

Try running 'task color white on red'.

jakob@MacBookAir ~ % task +DUETODAY list
No matches.
jakob@MacBookAir ~ % task add test  due:2024-10-11
Created task 3.
jakob@MacBookAir ~ % task +DUETODAY list
No matches.
jakob@MacBookAir ~ % task list

ID Age   Due        Description               Urg 
 2  3min 2024-10-11 Kochen                      12
 3 15s   2024-10-11 test                        12
 1  4min 2024-10-12 GP2-Excel proejec:uni       12

3 tasks
jakob@MacBookAir ~ % task due:202-11-10 list
Cannot subtract strings
jakob@MacBookAir ~ % task +due:202-11-10 list 
Cannot subtract strings
jakob@MacBookAir ~ % task +due:2024-11-10 list 
Cannot subtract strings
jakob@MacBookAir ~ % task list 

ID Age  Due        Description               Urg 
 2 4min 2024-10-11 Kochen                      12
 3 1min 2024-10-11 test                        12
 1 6min 2024-10-12 GP2-Excel proejec:uni       12

3 tasks
jakob@MacBookAir ~ % task 3 done
Completed task 3 'test'.
Completed 1 task.
jakob@MacBookAir ~ % task list

ID Age  Due        Description               Urg 
 2 4min 2024-10-11 Kochen                      12
 1 6min 2024-10-12 GP2-Excel proejec:uni       12

2 tasks
jakob@MacBookAir ~ % task done 1
Completed task 1 'GP2-Excel proejec:uni'.
Completed 1 task.
jakob@MacBookAir ~ % task add GP2-excel project:uni
Created task 3.
The project 'uni' has changed.  Project 'uni' is 50% complete (1 of 2 tasks remaining).
jakob@MacBookAir ~ % task project:uni list

ID Age   Project Description   Urg 
 2 13s   uni     GP2-excel        1

1 task
jakob@MacBookAir ~ % task +DUETODAY list
No matches.
jakob@MacBookAir ~ % task +WEEK list
No matches.
jakob@MacBookAir ~ % task WEEK öist
No matches.
jakob@MacBookAir ~ % task WEEK list
No matches.
jakob@MacBookAir ~ % task due:today list 
No matches.
jakob@MacBookAir ~ % task list

ID Age  Project Due        Description   Urg 
 1 9min         2024-10-11 Kochen          12
 2 3min uni                GP2-excel        1

2 tasks
jakob@MacBookAir ~ % task task 2 modify due:2024-10-12
No tasks specified.
jakob@MacBookAir ~ % task 2 modify due:2024-10-12 
Modifying task 2 'GP2-excel'.
Modified 1 task.
Project 'uni' is 50% complete (1 of 2 tasks remaining).
jakob@MacBookAir ~ % task list

ID Age   Project Due        Description   Urg 
 1 10min         2024-10-11 Kochen          12
 2  5min uni     2024-10-12 GP2-excel       13

2 tasks
jakob@MacBookAir ~ % ./taskwarrior-tui
zsh: no such file or directory: ./taskwarrior-tui
jakob@MacBookAir ~ % /Users/jakob/Downloads/taskwarrior-tui 
zsh: killed     /Users/jakob/Downloads/taskwarrior-tui
jakob@MacBookAir ~ % /Users/jakob/Downloads/taskwarrior-tui
zsh: killed     /Users/jakob/Downloads/taskwarrior-tui
jakob@MacBookAir ~ % brew install taskwarrior-tui
==> Downloading https://formulae.brew.sh/api/formula.jws.json
######################################################################### 100.0%
==> Downloading https://formulae.brew.sh/api/cask.jws.json
######################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/taskwarrior-tui/manifests/0.26.
######################################################################### 100.0%
==> Fetching taskwarrior-tui
==> Downloading https://ghcr.io/v2/homebrew/core/taskwarrior-tui/blobs/sha256:95
######################################################################### 100.0%
==> Pouring taskwarrior-tui--0.26.3.arm64_sequoia.bottle.tar.gz
==> Caveats
zsh completions have been installed to:
  /opt/homebrew/share/zsh/site-functions
==> Summary
🍺  /opt/homebrew/Cellar/taskwarrior-tui/0.26.3: 13 files, 4MB
==> Running `brew cleanup taskwarrior-tui`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
jakob@MacBookAir ~ % task list

ID Age   Project Due        Description   Urg 
 1 24min         2024-10-11 Kochen          12
 2 18min uni     2024-10-12 GP2-excel       13

2 tasks
jakob@MacBookAir ~ % taskwarrior-tui
jakob@MacBookAir ~ % ~/.zshrc
zsh: permission denied: /Users/jakob/.zshrc
jakob@MacBookAir ~ % cd
jakob@MacBookAir ~ % ~/.zshrc
zsh: permission denied: /Users/jakob/.zshrc
jakob@MacBookAir ~ % nano ~/.zshrc  # oder ~/.bashrc, je nach Shell
jakob@MacBookAir ~ % source ~/.zshrc  # oder source ~/.bashrc
jakob@MacBookAir ~ % tod
zsh: command not found: tod
jakob@MacBookAir ~ % jakob@MacBookAir ~ % nano ~/.zshrc  # oder ~/.bashrc, je nach Shell

zsh: command not found: jakob@MacBookAir
jakob@MacBookAir ~ % nano ~/.zshrc        
jakob@MacBookAir ~ % source ~/.zshrc
jakob@MacBookAir ~ % tt
Launching 'vi "task.cd0df198.task"' now...
Editing failed with exit code 256.
Launching 'vi "task.15a4aa93.task"' now...
Editing complete.
No edits were detected.
Launching 'vi "task.cd0df198.task"' now...
Editing complete.
Edits were detected.
Project modified.
jakob@MacBookAir ~ % notizen
jakob@MacBookAir Notizen % tt
jakob@MacBookAir Notizen % nano ~/.zshrc        
jakob@MacBookAir Notizen % source c 
source: no such file or directory: c
jakob@MacBookAir Notizen % cd
jakob@MacBookAir ~ % source ~/.zshrc        
jakob@MacBookAir ~ % td
2 files to edit
jakob@MacBookAir ~ % td
2 files to edit
jakob@MacBookAir ~ % notizen 
jakob@MacBookAir Notizen % jakobw
jakob@MacBookAir Jakob-Ws-github.io % vim assets/css/styles.css 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2018-08-20-bananas.md 
jakob@MacBookAir Jakob-Ws-github.io % pandoc /Users/jakob/Downloads/2024-29-10-primzahlen.html -o 2024-10-29-primzahlden.md                                     jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md 
jakob@MacBookAir Jakob-Ws-github.io % vim _includes/breadcrumbs.html 
jakob@MacBookAir Jakob-Ws-github.io % vim assets/css/styles.css 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim _includes/breadcrumbs.html      
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim assets/css/styles.css           
jakob@MacBookAir Jakob-Ws-github.io % vim _includes/breadcrumbs.html      
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim now.md 
jakob@MacBookAir Jakob-Ws-github.io % rm _posts/2018-08-20-bananas.md 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim _includes/navigation.html       
jakob@MacBookAir Jakob-Ws-github.io % vim _layouts/default
jakob@MacBookAir Jakob-Ws-github.io % vim _layouts/default.html
jakob@MacBookAir Jakob-Ws-github.io % cd
jakob@MacBookAir ~ % td
2 files to edit
jakob@MacBookAir ~ % jakobw
jakob@MacBookAir Jakob-Ws-github.io % vim _includes/breadcrumbs.html 
jakob@MacBookAir Jakob-Ws-github.io % vim now.md 
jakob@MacBookAir Jakob-Ws-github.io % vim about.md
jakob@MacBookAir Jakob-Ws-github.io % vim now.md  
jakob@MacBookAir Jakob-Ws-github.io % vin blog.md    
zsh: command not found: vin
jakob@MacBookAir Jakob-Ws-github.io % vin blog.md
zsh: command not found: vin
jakob@MacBookAir Jakob-Ws-github.io % vim blog.md 
jakob@MacBookAir Jakob-Ws-github.io % vim bue
jakob@MacBookAir Jakob-Ws-github.io % vim buecherregal.md 
jakob@MacBookAir Jakob-Ws-github.io % vim index.html 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md 
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim _posts/2024-10-29-primzahlden.md
jakob@MacBookAir Jakob-Ws-github.io % vim about.md 
jakob@MacBookAir Jakob-Ws-github.io % vim _layouts/buch.html
jakob@MacBookAir Jakob-Ws-github.io % vim buecherregal.md 
jakob@MacBookAir Jakob-Ws-github.io % vim /books/test.md

---
titel: tes
layout: buch
author: test
date: 2013-10-10
ratin: 10
---
ececse
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               

~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
-- INSERT --

