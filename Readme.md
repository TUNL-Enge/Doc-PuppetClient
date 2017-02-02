# Install notes

This assumes you have a clean install of Linux Mint (I'm using 17.3 KDE)

## Preparation

-   Install Linux Mint 17.3 from USB
-   Install puppet
    
        sudo apt-get install puppet
-   Make sure the "start" instruction is set automatically
    
        echo START=yes > puppet
        sudo mv puppet /etc/default/
-   Start the puppet service
    
        sudo /etc/init.d/puppet start

## Security

-   On the puppet server, sign the certificate
    
        sudo puppetca --sign engedaq-dev.physics.ncsu.edu