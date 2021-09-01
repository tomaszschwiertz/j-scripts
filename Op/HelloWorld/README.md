#Create a file

root@CE-A# run start shell

root@CE-A:# cd /var/run/scripts/op

root@CE-A:/var/run/scripts/op # touch op-hw.slax

cli


#Enable the Script

root@CE-A# set system scripts op file op-hw.slax


#How to fetch from a remote repository

run request system scripts refresh-from op file op-hw.slax url https://raw.githubusercontent.com/tomaszschwiertz/j-scripts/master/Op/HelloWorld/op-hw.slax

-or-

If you have this configured:

[edit system scripts op]
root@CE-A# show 
file op-hw.slax {
    source https://raw.githubusercontent.com/tomaszschwiertz/j-scripts/master/Op/HelloWorld/op-hw.slax;
}    

then, the easier refresh command would be as follows:

[edit system scripts op]
root@CE-A# set file op-hw.slax refresh


#How to run it

root@CE-A# run op op-hw.slax
