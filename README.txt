Here are two tiny utilities:

pty:            Run a script so that it thinks it is is connected to a
                terminal, and therefore flushes its output after every line. It
                solves the "line buffering problem".

timestamplines: Print all lines on STDIN to STDOUT but prepend a time stamp.

In concert, they allow you to timestamp the output of an arbitrary command like
so:

    $ pty some-command | timestamplines

or

    $ pty some-command | timestamplines -f > log &
    $ tail -f log

Also provided is slowprint to test it
