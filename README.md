This is a simple program for creating a diary, adding entries to a diary and producing a pdf
from the diary. 

Save the files diary, diary_new, diary_entry and diary_pdf together in their own folder.

To make diary executable from anywhere, add it's location to your PATH. 
Example:
    echo "export PATH=/usr/bin/diary:$PATH" >> ~/.bashrc

Where you choose to store the files and where you wish to prepend
to your PATH is up to you. In the above example, I added a folder to 
my /usr/bin called diary and have all the files there. 
I prepended to my PATH in my .bashrc, which is also where I store aliases
and other "custom" commands on my system. Your mileage may very. 

Also, add the man page (diary.man) to your MANPATH in order to call
the man page from anywhere. For instance, my man pages are located at
/usr/share/man, but yours may be different. 
You can run:
    $ sudo cp diary.man /usr/share/man/man1/diary.1
and then to access the manpage from anywhere:
    $ man diary

If you are unsure of your MANPATH one thing you might try (from ~ ):
    $ find ../../ | grep ".manpath"

Testing/bugs:
** MacOs:
    the command: $ diary pdf 
    fails on MacOs due to 'preconv' not existing.
    if this is the case, try updating groff with:
        $ brew install groff
    
** Archlinux:
    No problems yet.

** Windows:
    Ha! Never.

