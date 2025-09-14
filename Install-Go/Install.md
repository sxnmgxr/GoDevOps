1. Remove any previous GO installation by deleting the /usr/local/go folder (if it exists), then extract the archive you just downloaded into /usr/local, creating a fresh Go tree in /usr/local/go:

$ rm -rf /usr/local/go && tar -C /usr/local -xzf go1.25.1.linux-amd64.tar.gz

(You may need to run each command seperately with the neceassary permissions, as root or through sudo.)

Do not untar the archive into an existing /usr/local/go tree. this is known to produce broken Go installations.

2. Add /usr/local/go/bin to the PATH environment variables.
You can do this by adding the following line to your $HOME/.profile or /etc/profile (for a system-wide installation):

export PATH=$PATH:/usr/local/go/bin

Note: Changes made to a profile file may not apply until the next time you log into your computer. to apply the changes immediately, just run the shell commands directly or execute them from the profile using a command such as soruce $HOME/.profile

3. Verify that you've installed Go by opening prompt and typing the following command:
$ go version

4. Confirm that the command prints the installed version of Go.
