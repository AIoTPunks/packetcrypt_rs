# packetcrypt_rs - Super Good Announcement Mining Output

## Install
Step 1: If you haven't already done so, install rust.  [rustup](https://rustup.rs/)

Step 2: Enter the following command into your terminal/console.  

    git clone https://github.com/AIoTPunks/packetcrypt_rs
    cd packetcrypt_rs
    git checkout better-logging
    cargo build --release

> Here is a command step by step breakdown:
    
* This command downloads clones a copy of the github repository and installs it on your local machine.  [Further info](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

        git clone https://github.com/AIoTPunks/packetcrypt_rs
    
* This command navigates one layer down the directory into the "paketcrypt_rs" directory.

        cd packetcrypt_rs

* This command makes available and moves to the "better-logging" branch of the "packetcrypt_rs" code.

        git checkout better-logging
    
* This command compiles the code.

        cargo build --release
    

> Important if installing on windows.  In order to correctly compile the code you need to install specfic dependencies.  This instructions will guide you though that process.

[Windows 10 Installation Instructions](https://github.com/cjdelisle/packetcrypt_rs/issues/39#issuecomment-999982652)



## Mine Announcements

    ./target/release/packetcrypt ann http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7
    
*


    
(instead of pkt1xxx, use your wallet address)

For more information  `./target/release/packetcrypt ann --help`

To mine with visibility to error messages use the -e flag

    ./target/release/packetcrypt ann -e http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7

(instead of pkt1xxx, use your wallet address)


