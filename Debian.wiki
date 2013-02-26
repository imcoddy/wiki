Dynamic MMap ran out of room when trying to sudo apt-get anything

I believe one solution is just increase the value APT::Cache-Limit at the /etc/apt/apt.conf.d/70debconf, to do so use:

sudo gedit /etc/apt/aptt.conf.d/70debconf
and add the following to the end of the file:

APT::Cache-Limit "100000000";
..and then run:

sudo apt-get clean
sudo apt-get update --fix-missing
