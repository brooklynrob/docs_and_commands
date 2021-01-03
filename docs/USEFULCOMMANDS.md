---
id: usefulcommands
title: Useful Commands
sidebar_label: Useful Commands
slug: /usefulcommands
---



## This Site (Docusarus)
### Start the Site
In `/Users/robunderwood/Documents/workspace/DOCS`, run:
``` yarn run start```

## VirtualBox
### Connecting via ssh
#### Key Management
##### Generating Keys
[Instructions]
```

```
* Upload public key to [Google Compute](https://console.cloud.google.com/compute/metadata/sshKeys?project=elevated-watch-254300&folder&organizationId)


#### connect
```
ssh robunderwood@127.0.0.1 -p 2222
```

## [Google Cloud](https://console.cloud.google.com/compute/instances?project=elevated-watch-254300&instancessize=50&cloudshell=true)

### Managing [Google Cloud Instances](https://console.cloud.google.com/compute/instances?project=elevated-watch-254300&instancessize=50&cloudshell=true)



### [Key Management](https://console.cloud.google.com/compute/metadata/sshKeys?project=elevated-watch-254300&folder&organizationId)





### Connecting via ssh
```
ssh -i ~/.ssh/gcloud-ssh-key runderwood5@146.148.81.148
```


## Markdown
* [Github cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet): https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

  * [Using backticks in markdown](https://meta.stackexchange.com/questions/82718/how-do-i-escape-a-backtick-in-markdown): https://meta.stackexchange.com/questions/82718/how-do-i-escape-a-backtick-in-markdown

## Text Editing
### Cursor Commands
https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/ 
* Go to beginning of line: `C-a`
* Go to end of line: `C-e` 
* Option/Meta-F --> go forward one word
* Delete line: `C-e C-u`
[More handy terminal commands](https://stackoverflow.com/questions/9679776/how-do-i-clear-delete-the-current-line-in-terminal)

## emacs
### Basic commands
* Quit something `C-g`
* Get help `C-h i`
* See key bindings `C-h b`
* View directory `M-x dired`


Get help           C-h  (Hold down CTRL and press h)
Emacs manual       C-h r        Browse manuals     C-h i
Emacs tutorial     C-h t        Undo changes       C-x u
Buy manuals        C-h RET      Exit Emacs         C-x C-c
Activate menubar   M-`

### Scrolling
* Go FORWARD one WORD `M-f`
* Go BACKWARD one WORD `M-b`
* Go FORWARD one LINE `C-n`
* Go BACKWARD one LINE `C-p`
* Move forward one screenful C-v	
* Move backward one screenful M-v	
* Move to start of buffer M-< (M-Shift-,) 
* Move to end of buffer M-> (M-Shift-.) 
* Clear screen and redisplay all the text, moving the text around the cursor to the center of the screen. C-l	 (That's CONTROL-L, not CONTROL-1.)

### Text editing
Killing and Deleting   backward   forward

* character        `DEL`    or `C-d`
* word             `M-DEL`  or `M-d`
* line (to end of) `M-0 C-k` or    `C-k`
* sentence         `C-x DEL`     `M-k`
* sexp             `M-- C-M-k` or `C-M-k`


Type C-l to begin editing.

Get help           C-h  (Hold down CTRL and press h)
Emacs manual       C-h r
Emacs tutorial     C-h t           Undo changes     C-x u
Buy manuals        C-h C-m         Exit Emacs       C-x C-c
Browse manuals     C-h i
Activate menubar   F10  or  ESC `  or   M-`
(`C-' means use the CTRL key.  `M-' means use the Meta (or Alt) key.
If you have no Meta key, you may instead type ESC followed by the character.)



* Set a mark `C-SPC` or `C-@`

### Bash / Shell
* Open Bash `M-x bash`

### Buffers and Windows
#### Buffers
* Close (Kill) Buffer `C-x k`
* select another buffer `C-x b`
* list all buffers `C-x C-b`
* Re-evaluate whole buffer `M-x eval-buffer`
* Evaluate single expression in file `C-c C-e`
* Compile current entire file with REPL section `C-c C-k`
* Split Window vertically `C-x 2`
* Split Window to right (split-window-right) `C-x 3`
* Close Current Window `C-x 0`
* Move to other window `C-x O`

[More Created and Selecting Buffers](https://www.gnu.org/software/emacs/manual/html_node/emacs/Select-Buffer.html)




### Themes
* customize-themes `M-x`


### Query
* Query (Find and Replace): `M-%` (`M and Shift 5`)
  * `Spc` or `Y` to replace and go to next one



### Emacs term mode
Start Term Mode: `M-x term`

Switching modes in term mode - (from [GNU](https://www.gnu.org/software/emacs/manual/html_node/emacs/Term-Mode.html)):

* `C-c C-j`:
Switch to line mode (term-line-mode). Do nothing if already in line mode.


* `C-c C-k`: Switch to char mode (term-char-mode). Do nothing if already in char mode.


### emacs 4 pane setup for OCaml

![Emacs 4 pane setup for OCaml](/img/emacs-setup-ocaml.png)


### Language Specific Emacs Stuff
#### Emacs Lisp (Elisp)
[Video: Zamansky  - Using Emcacs - lesson 3 Elisp](https://www.youtube.com/watch?v=nyQxRarVYH4)
[Video: Programming in LISP 0 (Slime, clisp, emacs )](https://www.youtube.com/watch?v=UtGLp8jG7gY)

##### Installation
Linux (e.g. Ubuntu): `sudo apt-get install emacs clisp slime`

From folder in which quicklisp.lisp exists: `clisp -i ./quicklisp.lisp`
... then, from within Lisp
* `(quicklisp-quickstart:install)`
* `(ql:add-to-init-file)`
* `(ql:quickload "quicklisp-slime-helper")`


#### Using slime
* `M-x slime-compile-region`


#### Clojure - Cider
* Open a new repl: M-x cider-jack-in
  or C-c M-J

  remove any meniton of cider-nrepl from ~/.lein/profiles.clj

#### OCaml (Tuareg / Merlin)
Emacs OCaml mode is available via [Tuareg](https://github.com/ocaml/tuareg)
* Open a new repl `M-x run-ocaml`
  * `OCaml repl to run: utop`

##### `opam-user-setup`
Great tool. See its [Github repo](https://github.com/OCamlPro/opam-user-setup)


### Reloading and Evaluation
#### Evaluate
* Evalate expression: `C-c C-e`

##### Reload File
From https://stackoverflow.com/questions/2580650/how-can-i-reload-emacs-after-changing-it
```
You can use the command load-file (M-x load-file, then press return twice to accept the default filename, which is the current file being edited).

You can also just move the point to the end of any sexp and press C-xC-e to execute just that sexp. Usually it's not necessary to reload the whole file if you're just changing a line or two.
```



## Unix / Bash
### Send stdout to both console and a file
Format: `foo | tee output.file`
Example: `create-react-app sandbox-reason --scripts-version reason-scripts | tee ../../COMMANDS-and-LOGS/react/create-react-app_sandbox-reason_2017_11_23`

### Find File
* See https://apple.stackexchange.com/questions/82218/show-hidden-files-when-searching-in-finder
* Example: `sudo find . -name ".merlin" | tee ~/workspace/workspace-gd/COMMANDS-and-LOGS/ocaml/lots-of-.merlins_2018-12-27.log`

### Setting environment variables
https://flaviocopes.com/shell-environment-variables/

### Reload bash_profile file
https://stackoverflow.com/questions/4608187/how-to-reload-bash-profile-from-the-command-line


### `ln` command - links (hard or symbolic)
* Example: ```ln /CS_Book/USEFULCOMMANDS.md /COMMANDS-and-LOGS/USEFULCOMMANDS.md```

## Git (and Github)
* SSH
	* [Github Guide](https://help.github.com/articles/checking-for-existing-ssh-keys/)
* Show branches
	* `git branch`
	* (To see last commit on each bracnh) `git branch -v`
	* (Just show merged branches) `git branch --merged`
	* (Just show unmerged branches) `git branch --no-merged`
	* [More Info](https://git-scm.com/book/en/v2/Git-Branching-Branch-Management)

* Show remotes
  * `git remote -v`

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
		* See https://stackoverflow.com/questions/4372435/how-can-i-rollback-a-github-repository-to-a-specific-commit

``` brooklynrobmac:alloy robunderwood$ git reset --hard bb8fc1a447cacf1dfb0271a4c9b86c288ddc4c70
			HEAD is now at bb8fc1a fix finos watermark (#254)
			brooklynrobmac:alloy robunderwood$ git push -f origin master
			Total 0 (delta 0), reused 0 (delta 0)
			To github.com:brooklynrob/alloy.git
			+ db291d8...bb8fc1a master -> master (forced update)
```
* Remove a file from a pull request / go back to a particular file version
	* https://stackoverflow.com/questions/39459467/remove-a-modified-file-from-pull-request
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

* Pull from upstream flow
	* `git remote add upstream git@github.com:finos/alloy`
	* `git pull upstream master`
	* `git merge upstream/master`


# Python
* check version: `python --version`

## pyenv
* Maintain multiple versions of python (similar to nvm or opam switch)
* https://realpython.com/intro-to-pyenv/

## pipenv
* https://realpython.com/pipenv-guide/
* virtual envs created by pipenv are in `/Users/robunderwood/.local/share/virtualenvs/`

![pyenv_shortcut_pipenv.png](/img/pyenv_shortcut_pipenv.png)



## Python
* check version: `python --version`


### Jupyter Notebook
#### Running the Notebook
['Running the Notebook' Documentation](https://jupyter.readthedocs.io/en/latest/running.html#running)

At command line:
```jupyter notebook```
Or to open to other computers on network
```jupyter notebook --ip=0.0.0.0```

### Jupyter Lab
#### [Install Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)
* 'pip install jupyterlab'
#### Running
* Run
	* `pipenv shell`
	* `jupyter lab
* exit: `exit`

### Pandas
#### Load a CSV and Display the Columns
```
df_csv = pd.read_csv('pokemon_data.csv')
print(df_csv.columns)
```

### Perspective Python
* Dependencies 
  * NPM
    * [Install NPM On Ubuntu](https://tecadmin.net/install-latest-nodejs-npm-on-ubuntu/)
      * `sudo apt-get install nodejs`
* Install Perspective
* Install Perspective Python


### VirtualEnv
#### Turn Off
* `deactivate`




## OCaml
### package manager - opam -  use
* list installed and avail releases of OCaml
	* `opam switch`
	* Example: `open switch realworld`
![opam switch](/img/opam_switch_list_pwd.png)
* Put environment in synch: ``eval `opam config env` ``

### Location of ocaml compiliers
* `/Users/robunderwood/.opam`
  * e.g., `/Users/robunderwood/.opam/4.11.1`

### Location of ocaml config file
* `~/.ocamlinit`

### UTOP
#### `#require` then `open` a library
Example (not lowercase and then capital letter):
```	
#require "base";;
open Base;;
```
Another example:
```
#require "async";;
open Async;
```

### `ocamlbuild` examples
* `ocamlbuild -pkg cohttp-lwt-unix -pkg lwt_ssl get_json_data.byte get_json_data.ml && ./get_json_data.byte`

### Dune / JBuilder


### OCaml syntax Stuff

### Differences between stdlib and Jane Street
Big difference: Jane Street uses labelled arguements
```
utop # List.map
- : ('a -> 'b) -> 'a list -> 'b list = fun

utop # List.map (fun x -> x + 1) [5;6];;
- : int list = [6; 7]

utop # open Base;;

utop # List.map;;
- : 'a list -> f:('a -> 'b) -> 'b list = fun

utop # List.map (fun x -> x + 1) [5;6];;
Error: This expression should not be a function, the expected type is
utop # List.map ~f:(fun x -> x + 1) [5;6];;
- : int list = [6; 7]
```

The following (from [problem 8 in OCaml 99 problems](https://ocaml.org/learn/tutorials/99problems.html)) works with the stdlib:
```utop # let rec compress = function
    | a :: (b :: _ as t) -> if a = b then compress t else a :: compress t
    | smaller -> smaller;;
val compress : 'a list -> 'a list = <fun>

utop # compress ["a";"a";"a";"a";"b";"c";"c";"a";"a";"d";"e";"e";"e";"e"];;
- : string list = ["a"; "b"; "c"; "a"; "d"; "e"]
```

but with Jane Street Base, which has removed polymorphic compare, you need to do this

```
utop # let rec compress = function
    | a :: (b :: _ as t) -> if (String.equal a b) then compress t else a :: compress t
    | a -> a;;
val compress : string list -> string list = <fun>

utop # compress ["a";"a";"a";"a";"b";"c";"c";"a";"a";"d";"e";"e";"e";"e"];;
- : string list = ["a"; "b"; "c"; "a"; "d"; "e"] 
```



#### List
##### `List.fold_left`
`List.fold_left` - Jane Street (Core) Syntax:
  ```
  List.fold_left ~init:0 ~f:(fun acc x -> acc + x) [2; 5; 7];;
  ```

`List.fold_left` - Standard OCaml (4.04.2):
  ```
  List.fold_left (fun acc x -> acc + x) 0 [2; 5; 7];;
  ```

`List.fold_left` - ReasonML 3.2.0
  ```
  List.fold_left((acc, x) => acc + x, 0, [2, 5, 7]);
  ```

`List.fold_left` - longer example (Core style):

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

Example: 
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

##### meaning of `[@@deriving sexp]
Deriving a way to add syntax extension to OCaml

Deriving sexp adds a set of functions to a custom type to allow ready conversion to/from S-expressions (Symbolic Expressions)

```
utop # open Sexplib.Std;;
utop # open Ppx_sexp_conv;;

utop # type t = { foo: int; bar: float } [@@deriving sexp];;
type t = { foo : int; bar : float; }
val t_of_sexp : Sexplib0.Sexp.t -> t = <fun>
val sexp_of_t : t -> Sexplib0.Sexp.t = <fun>

utop # let tst = { foo = 1; bar = 1.0 };;
val tst : t = {foo = 1; bar = 1.}

let tst_sym = sexp_of_t tst;;
val tst_sym : Sexplib0.Sexp.t = ((foo 1) (bar 1))
```


##### meaning of `open!`
* See https://caml.inria.fr/pub/docs/manual-ocaml-4.01/extn.html#sec236
	* It's to suppress warnings of shadows

### ReasonML
#### Reprocessing
* https://github.com/bsansouci/reprocessing-example

## Jupyter-OCaml
From Sept 2020
See https://github.com/akabe/ocaml-jupyter
```
cp /Users/robunderwood/.opam/4.07.1/share/jupyter/kernel.json /Users/robunderwood/.opam/jupyter-ocaml/share/jupyter/kernel.json

cp jupyter-ocaml robunderwood$ cp /Users/robunderwood/.opam/4.07.1/share/jupyter/kernel.sh /Users/robunderwood/.opam/jupyter-ocaml/share/jupyter/kernel.sh
```

```
ls -a ~/Library/Jupyter/kernels/ocaml-jupyter/
```

```
brooklynrobmac:jupyter-ocaml robunderwood$ ls /usr/local/share/jupyter/kernels/ocaml-jupyter/
kernel.json	kernel.sh
```


## Clojure
```
$ lein uberjar

$ java -jar   /Users/robunderwood/workspace/cllied/target/cljapplied-0.1.0-SNAPSHOT-standalone.jar

Clojure 1.7.0
user=>  (require 'ch1.validate)
nil
user=> (in-ns 'ch1.validate)
#object[clojure.lang.Namespace 0x46b61c56 "ch1.validate"]
ch1.validate=> (in-ns 'user)
#object[clojure.lang.Namespace 0xbcef303 "user"]
user=>
```


### Syntax
#### Map
`(map (fn [name] (str "Hi, " name)) ["Darth" "Mr. Magoo"])`
can be shortened to:
`(map #(str "Hi, " %) ["Darth" "Mr. Magoo"])`
another example:
`(map #(* % 3) '(8 4))`
Compared this with OCaml (Jane Syntax): 
```
List.map ["Darth"; "Mr. Magoo"] (fun s -> String.concat ["Hi, "; s]);;
- : string list = ["Hi, Darth"; "Hi, Mr. Magoo"]
```

Returning functions

```
user=> (defn sub-maker
  #_=> "Create a customer decrementor"
  #_=> [sub-by]
  #_=> #(- % sub-by))
#'user/sub-maker
user=> (def sub3 (sub-maker 3))
#'user/sub3
user=> (sub3 5)
2
```

## Destructuring in Clojure
```
user=> (let [[head & tail] [1 2 3]] head)
1
user=> (let [[head & tail] [1 2 3]] tail)
(2 3)
```







## Ruby
### Rails



## Databases
### PostgreSQL
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


## Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List


You can use the [editor on GitHub](https://github.com/finos-data-tech/finos-data-tech.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/finos-data-tech/finos-data-tech.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
