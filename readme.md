# packetcrypt_rs
PacketCrypt implementation in Rust

## What exists
PacketCrypt mining is made up of 6 distinct components:
* Master - provides work and config files to everyone for a given pool
* Announcement Miner - generates announcements (data which uses bandwidth)
* Announcement Handler - consumes announcements, checks validity and provides to block miner
* Block Miner - uses announcements for for mining blocks
* Block Handler - takes shares from Block Miner and validates them
* Paymaker - takes messages from Block Handler and Announcement Handler to
decide which miners the pool should pay

The Master, Announcement Handler, Block Handler, and Paymaker must be operated
by the mining pool, the Announcement Miner and Block Miner can be operated by 3rd
parties.

This codebase currently provides the *Announcement Handler* and *Announcement Miner* components.
All of the others can be found in
[the C PacketCrypt project](https://github.com/cjdelisle/PacketCrypt).

## Install
First install rust if you haven't, see: [rustup](https://rustup.rs/)

    git clone https://github.com/AIoTPunks/packetcrypt_rs
    cd packetcrypt_rs
    git checkout better-logging
    cargo build --release

[Windows 10 Installation Instructions](https://github.com/cjdelisle/packetcrypt_rs/issues/39#issuecomment-999982652)

These instructions are important if installing on windows.  In order to correctly compile the code you need to install specfic dependencies.

## Mine Announcements

    ./target/release/packetcrypt ann http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7
    
(instead of pkt1xxx, use your wallet address)

For more information  `./target/release/packetcrypt ann --help`

To mine with visibility to error messages use the -e flag

    ./target/release/packetcrypt ann -e http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7

(instead of pkt1xxx, use your wallet address)


