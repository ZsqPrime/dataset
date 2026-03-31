# wi: a simple git-based wiki

wi is a super simple CLI wiki.  Pages are plain text files stored in a git
repo.  You edit pages using your favourite text editor (`$EDITOR`, or vim
by default).

## Getting started

Edit a page:

    $ wi todo
    Initialized empty Git repository in /Users/rob/tmp/wi/.git/
    [master (root-commit) 3630b5b] todo create
     1 file changed, 4 insertions(+)
     create mode 100644 docs/todo.md

wi spawns vim where you make your changes.  Save the file in your editor
and quit.  This creates a new file in git and commits it.

    $ wi meeting-minutes
    [master 177951f] meeting-minutes create
     1 file changed, 3 insertions(+)
     create mode 100644 docs/meeting-minutes.md

Update an existing topic:

    $ wi todo
    [master 37aa1b3] todo update
     1 file changed, 1 insertion(+), 1 deletion(-)

wi spawns vim where you make your changes.  Save the file in your editor
and quit.  This updates the todo topic file in git and commits it.  If no
changes were made to the file, no git commit is made.

List wiki topics:

    $ wi --ls
    meeting-minutes
    todo

And everything is stored in git:

    $ cd $WI_PATH/docs
    $ ls
    meeting-minutes.md todo.md
    $ git branch
    * master
    $ git log --graph --pretty=oneline --abbrev-commit
    * 37aa1b3 todo update
    * 177951f meeting-minutes create
    * 3630b5b todo create


## wiki location

You can set the location of your wiki with the `$WI_PATH` environment
variable, or `$HOME/.wi/wiki` by default.


## bash completion

source `bash_completion` to get tab completion for wiki topics.

    $ wi <tab>
    --list           meeting-minutes  todo

## License

MIT.  See "LICENSE.txt".
