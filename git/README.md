# Git Cheatsheet

## Squashing
`$ git rebase -i HEAD~{number of commits}`

In vim find and replace `pick` with `s` except the first one.
Find and replace like so: `:%s/pick/s`  
