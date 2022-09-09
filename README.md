# screenshot-i3
A simple script for taking screenshots in i3wm using the prtscr button. You are going to need the packages `xclip` and `imagemagick`

Firstly save the script as `~/.screenshot-i3.sh`. You need to set the script as executable like this:

    chmod 755 ~/.screenshot-i3.sh
  
Now create a symlink to the script:

    cd /usr/bin
    
<!-- asdf -->

    sudo ln -s /home/username/.screenshot-i3.sh screenshot-i3  

Now edit your i3 configuration file:

    nano ~/.config/i3/config

And add these lines to the bottom:

    # take a screenshot of a screen region and copy it to a clipboard
    bindsym --release Shift+Print exec "screenshot-i3 -s /home/username/Pictures/screenshots/"

    # take a screenshot of a whole window and copy it to a clipboard
    bindsym --release Print exec "screenshot-i3 /home/username/Pictures/screenshots/"
    
And you should be good to go 👍
