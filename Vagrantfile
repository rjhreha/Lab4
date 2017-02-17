#!/bin/bash

# Script to add a user to Linux system

if [ $(id -u) -eq 0 ]; then

read -p "Enter username : " username

read -s -p "Enter password : " password

egrep "^$username" /etc/passwd >/dev/null

if [ $? -eq 0 ]; then

echo "$username exists!"

exit 1

else

pass=$( HYPERLINK "http://unix.stackexchange.com/questions/125726/important-scripts-useful-for-a-linux-system-administrator" perl -e 'print crypt($ARGV[0], "password")' $password)

useradd -m -p $pass $username

[ $? -eq 0 ] && echo "User has been added to system!" || echo "Failed to add a user!"

fi

else

echo "Only root may add a user to the system"

exit 2

fi
 ##this may work well Richard!!
