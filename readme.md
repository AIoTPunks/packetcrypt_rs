# packetcrypt_rs - Super Good Announcement Mining Output

## Install
Step 1: If you haven't already done so, install rust.  [rustup](https://rustup.rs/)

Step 2: Enter the following command into your terminal/console.  

    git clone https://github.com/AIoTPunks/packetcrypt_rs
    cd packetcrypt_rs
    git checkout better-logging
    cargo build --release

Command step by step breakdown:
    
    git clone https://github.com/AIoTPunks/packetcrypt_rs

2) [Windows 10 Installation Instructions](https://github.com/cjdelisle/packetcrypt_rs/issues/39#issuecomment-999982652)

These instructions are important if installing on windows.  In order to correctly compile the code you need to install specfic dependencies.

## Mine Announcements

    ./target/release/packetcrypt ann http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7
    
(instead of pkt1xxx, use your wallet address)

For more information  `./target/release/packetcrypt ann --help`

To mine with visibility to error messages use the -e flag

    ./target/release/packetcrypt ann -e http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7

(instead of pkt1xxx, use your wallet address)


