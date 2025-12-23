1. route setup incomplete ❌
2. cluster connect ✅
3. mongodb installed done ✅
4. firebase and mongodb connect and secure both client and server site secure ✅
5. .env user name and password set kora hoy niii
6. ! firebase.configaration is incomplete - cant secure (.env.local)❌
7. ERROR DETAILS PAGE
8. submit_type: null, WHAT IS IT
9. membership db - dublicate data sent
10. what is payment id - add in my club payment id
11. event - how to set db
12. membership or event payment type ❌
13. error : AddEventForm - catagories managerClubs dublicate
14. error : AddEventForm - ClubName
15. events details page - join toast not working
16. jwt cannot set - loading page
17. vercel deploy and connect github how?
18.
19.

---

extra feature :

1.  add local stogare facility for club join and dissable button

---

learn :

1. useMutation hook case :
2. hooks > useRole : Custom hook

---

1+2 file explain.
3 react hook form - signup page
4 react hook form - img

---

my orders : my clubs - member -
my inventory : manager club create or manage - manage club - from clubsCollection
manage orders : manager club member - admin/no-manager - my club - need approve of admin

admin - statistics , manage users
customer - statistics , my orders , become a seller
seller - statitics ,

---

Step 1: In your Git Bash terminal, type this and press Enter:
`notepad ~/.bashrc`
Step 2: Notepad will open. Add this line at the very bottom:

- for file name with user name:
  `xport PROMPT_DIRTRIM=2`
  or
  `PS1='\u@\h $MSYSTEM \[\033[36m\]\W\[\033[0m\]\n\$ '`

- for user name only with style :
  ` PS1="\[\033[32m\]\u@\h \[\033[35m\]$MSYSTEM \[\033[0m\]\$ "`

- for user name only , no-style :
  `PS1='\u@\h $MSYSTEM\n\$ '`
- for file name
  `PS1='\u@\h $MSYSTEM \[\033[36m\]\W\[\033[0m\]\n\$ '`
- for username and 2 folder name :
  ````PROMPT_COMMAND='SHORT_PATH=$(pwd | grep -o "[^/]*/[^/]*$")'
  PS1='\u@\h $MSYSTEM /\[\033[36m\]$SHORT_PATH\[\033[0m\]\n\$ ' ```
  ````
- for custom message :
  `parse_git_branch() {
  git branch 2>/dev/null | grep '*' | sed 's/* //'
}
PROMPT_COMMAND='SHORT_PATH=$(pwd | grep -o "[^/]*/[^/]*$")'
PS1='\[\033[35m\]⚡ Keep Coding\[\033[0m\] | \[\033[36m\]$SHORT_PATH\[\033[0m\] \[\033[33m\]$(parse_git_branch)\[\033[0m\] \$ '`

claude link : https://claude.ai/share/ac61623e-3a54-4617-9855-36f0692b6005
