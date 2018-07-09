# mog-ip-install.sh

This will setup 3 MOG MNS on a VPS with 3 IPS, you will be required to enter the 3 IPS when asked for each MN. It will also create a systemlink.


#Adds syslink (done for you in script)

systemctl enable mogwai.service

systemctl enable mogwai2.service 

systemctl enable mogwai3.service

#Starts the MNs (done for you in script)

systemctl start mogwai.service

systemctl enable mogwai2.service

systemctl enable mogwai3.service

#Check status of MNS

mogwai-cli mnsync status (MN1)

mogwai-cli -datadir=/root/.mogwaicore2 mnsync status (MN2)

mogwai-cli -datadir=/root/.mogwaicore3 mnsync status (MN3)

mogwai-cli masternode status (MN1)

mogwai-cli -datadir=/root/.mogwaicore2 masternode status (MN2)

mogwai-cli -datadir=/root/.mogwaicore3 masternode status (MN3)
