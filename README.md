# Debian (and Debian based systems) kernel source & realtek wifi driver update
instructions to update the kernel header for a custom kali linux kernel + realtek wifi driver install (requires kernel update)


    sudo apt -y update && sudo apt -y upgrade

    sudo apt install -y linux-headers-$(uname -r) build-essential bc dkms git libelf-dev rfkill iw

    sudo reboot now

For nineplus AC1200 wireless card (capable of packet injection)


    mkdir -p ~/src

    cd ~/src

    git clone https://github.com/morrownr/88x2bu-20210702.git

    cd ~/src/88x2bu-20210702

    sudo ./install-driver.sh

Allow the installer to reboot your system. Afterwards, execute the following to update the driver when needed:


    sudo sh install-driver.sh
