MusicBox turns your RaspberryPi and a MIDI keyboard into a Synthesizer!

Installation:
__ansible-playbook -i "*SERVER_IP* ," -u *REMOTE_USER* --ask-pass --ask-become-pass musicbox.yml__ 

The used soundfont can be changed in the file *fluidsynth.service* at the end of the *ExecStart=*-line.
Currently the script is expecting this soundfont: http://schristiancollins.com/generaluser.php

Probably you have to change the soundcard/device, as you might have different hardware.
The default soundcard is set in *musicbox.yml* in the *Change default sound card*-parts.
Also, jack is set to use that soundcard in *jackd.service* in its *ExecStart=*-line.

The file *commands.txt* contains some useful commands to work with audio hardware in linux.