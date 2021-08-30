#Create a file

root@CE-A# run start shell

root@CE-A:# cd /var/run/scripts/op

root@CE-A:/var/run/scripts/op # touch op-hw.slax

cli


#Enable the Script

root@CE-A# set system scripts op file op-hw.slax


#How to fetch from a remote repository

run request system scripts refresh-from op file op-hw.slax url https://raw.githubusercontent.com/tomaszschwiertz/j-scripts/master/Op/HelloWorld/op-hw.slax


#How to run it

root@CE-A# run op op-hw.slax
