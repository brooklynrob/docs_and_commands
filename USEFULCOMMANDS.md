# Markdown
* Github cheatsheet: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

# Text Editing
## Cursor Commans
https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/ 
* Ctrl-A --> beginning of line
* Ctrl-E --> end of line
* Option/Meta-F --> go forward one word

# Useful Commands (Unix / Bash)
## Send stdout to both console and a file
foo | tee output.file
create-react-app sandbox-reason --scripts-version reason-scripts | tee ../../COMMANDS-and-LOGS/react/create-react-app_sandbox-reason_2017_11_23

## Find File
* See https://apple.stackexchange.com/questions/82218/show-hidden-files-when-searching-in-finder
* Example: `sudo find . -name ".merlin" | tee ~/workspace/workspace-gd/COMMANDS-and-LOGS/ocaml/lots-of-.merlins_2018-12-27.log`


## `ln` command - links (hard or symbolic)
* Example: ```ln /CS_Book/USEFULCOMMANDS.md /COMMANDS-and-LOGS/USEFULCOMMANDS.md```

# Git (and Github)
* SSH
	* [Github Guide](https://help.github.com/articles/checking-for-existing-ssh-keys/)
* Show branches
	* `git branch`
	* (To see last commit on each bracnh) `git branch -v`
	* (Just show merged branches) `git branch --merged`
	* (Just show unmerged branches) `git branch --no-merged`
	* [More Info](https://git-scm.com/book/en/v2/Git-Branching-Branch-Management)

* Show branches on the remote origin repo (e.g. Github)
	* `git remote show origin`

* Show branches on the remote upstream - the repo that origin was forked FROM
	* `git remote show upstream`

* Show all branches, both local and remote
	* `git branch -a`
	* [More info on remote branches](http://gitready.com/intermediate/2009/02/13/list-remote-branches.html)

* Show commit history
	* `git log`
	* [More Info on viewing commit history](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History)

* (Hard) reset to previous commit
	* `git reset --hard <commithash>`

* Add upstream repository
	* `git remote add upstream git@github.com:sketch-city/harvey-api.git`

* Show upstream
	* `git remote show upstream`

* Get a new branch from the upstream repository
	* `git checkout -t upstream/<new branch>`

* Push that new branch to your/origin/forked repository
	* `git push origin <that new branch>`

* Delete remote branch
	* `git push origin --delete rfu001`


## Language Specific (Syntax and Env Setup)
### ocaml
#### package manager - opam -  use
* list installed and avail releases of OCaml
	* `opam switch`
	* Example: `open switch realworld`
* Put environment in synch: `eval `opam config env``

#### UTOP
##### `#require` then `open` a library
Example (not lowercase and then capital letter):
	```	
		#require "base";;
		open Base;;
	```

	```
		#require "async";;
		open Async;
	```

#### `ocamlbuild` examples
* `ocamlbuild -pkg cohttp-lwt-unix -pkg lwt_ssl get_json_data.byte get_json_data.ml && ./get_json_data.byte`


#### OCaml syntax Stuff
##### List
###### `List.fold_left`
Example:
  ```
  List.fold_left ~init:0 ~f:(fun acc x -> acc + x) [2; 5; 7];;
  ```

  ```
  utop # let concat (l : string list) : string =
  List.fold_left ~f:(fun acc x -> acc ^ " " ^ x) ~init:"" l;;
  val concat : string list -> string = <fun>
  utop # concat ["hello"; "Rob"];;
  - : string = " hello Rob"
  ```

##### meaning of `<` mean
	https://ocaml.org/learn/tutorials/labels.html
		Take a careful look at the type of that function. Type inference has worked out that the st argument has type [< `Close | `Open]. The “<” (less than) sign means that this is a closed class. In other words, this function will only work on `Close or `Open and not on anything else.

##### meaning of `let@bind`
Shorthand to make bind look/act like a normal `let` statement

##### meaning of `@@`
See https://www.reddit.com/r/ocaml/comments/3qmapa/operator/
`('a -> 'b) -> 'a -> 'b = <fun>`

	```
		utop # (@@);;
		- : ('a -> 'b) -> 'a -> 'b = <fun>
		utop # let addone x = x + 1;;
		val addone : int -> int = <fun>
		utop # let addtwo x = x + 2;;
		val addtwo : int -> int = <fun>
		utop # addtwo(addone(4));;
		- : int = 7
		utop # addtwo@@addone 4;;
		- : int = 7
	```

##### meaning of `open!`
* See https://caml.inria.fr/pub/docs/manual-ocaml-4.01/extn.html#sec236
	* It's to suppress warnings of shadows

#### ReasonML
##### Reprocessing
* https://github.com/bsansouci/reprocessing-example



## Clojure

## Ruby
### Rails



# Databases
## PostgreSQL
* Start the server
	* `pg_ctl -D /usr/local/var/postgres -l logfile start`
	or
	* `brew services start postgresql`

* Create a new user with a password
	* `createuser <username> -P`

* start psql with a specific user
	* `psql -U <username`

* quit psql
	* `\q`
