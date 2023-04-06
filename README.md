# vtoyboot
Backup for the script that makes a Linux install fully portable VHD/VDI on Ventoy.

# How
Just extract the .tar.gz file then run it with `sh ventoyboot.sh`

**NOTE:** You **must** run this script everytime you do an upgrade, change drivers or install a new kernel, initramfs...

# Why
I've been looking for this script a whole week. It's not only stupidly hidden enough but also undocumented for similar nonsensical reasons...

Let's say you want to create a fully portable Linux installation with the next features:
- Full real 100% install on disk, not some live-cd bulls**t.
- Bootable on any computer, even with SecureBoot enabled.
- Packed into a single binary virtual disk file (VHD, VDI, etc).

Ventoy is a great Boot Manager that allows to do exactly all of this. Supports lots of Operating Systems, many architectures.
One of its best features is to be able to boot installed systems contained in a single file, using popular virtual disk file formats.
This opens lots of new possibilities for a more secure, distributed computing. Now we have a way to keep our OS'es clean and fresh everytime.

**SPOILER: Rant below**

Now, for the Linux approach, running a certain script is needed during the process.
You follow the instructions, go to the repo, extract the package and... 

> NO FILE???!!!

You check again that repository. There are 3 files only:
- an ISO FILE, which seems to be a live-cd or something.
- a .tar.gz package. *(Ah! It must be this file!)*
- a .zip file. *(Maybe it's there?)*

> Wait a minute... 
- No trace of the script anywhere.
- No script found inside the .zip file.
- No script found inside the .tar.gz file.
- The contents of the .zip and the .tar.gz files matches, they're both the same...
- The contents of the ISO file matches with those of the .tar.gz above...

> Guess what?
The right script is ONLY included inside thay .tar.gz file... INSIDE THAT ISO!!!

So I decided to backup just the needs and upload to my own repo, for the good of mankind.
