# packetcrypt_rs - Super Good Announcement Mining Output

## Install
Step 1: If you haven't already done so, install rust and git -  [rust](https://rustup.rs/), [git](https://github.com/git-guides/install-git)

Step 2: Enter the following command into your terminal/console.  

    git clone https://github.com/AIoTPunks/packetcrypt_rs
    cd packetcrypt_rs
    git checkout better-logging
    cargo build --release

> Command step by step breakdown:
    
* This command clones a copy of the github repository and installs it on your local machine.  [2.1 Git Basics - Getting a Git Repository](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

        git clone https://github.com/AIoTPunks/packetcrypt_rs
    
* This command navigates one layer down your directory into the "paketcrypt_rs" directory.

        cd packetcrypt_rs

* This command makes available and moves to the "better-logging" branch of the "packetcrypt_rs" code.

        git checkout better-logging
    
* This command compiles the code.

        cargo build --release
    

> Important if installing on windows.  In order to correctly compile the code you need to install specfic dependencies.  This instructions will guide you though that process.

[Windows 10 Installation Instructions](https://github.com/cjdelisle/packetcrypt_rs/issues/39#issuecomment-999982652)



## Mine Announcements

    ./target/release/packetcrypt ann http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7
    
* Ensure that you enter this command from the "packetcrypt_rs" directory.  The "./target/release" part of the command starts in the "packetcrypt_rs" dirctroy and drills down into the "target" directory and then into they "release" directory.

* Announcement mining can be done into a single pool or into multiple pools. You can mine in as many pools as you have the bandwidth to supply.
 When you announcement mine into multiple pools, you will be paid by each pool that you submit annoucements to.  The first pool is the pool running the highest difficulty. If you notice problems, you can test listing the pools in a different order. If a pool is down or malfunctioning you will notice the pool not mining at [100%] with the following color scheme: Green >75%, Yellow 50% - 75%, Red <50%. You can choose to remove the under-performing or malfunctioning pool(s).  
  
* (instead of pkt1xxx, use your wallet address)

* For more information  `./target/release/packetcrypt ann --help`

* To mine with visibility to error messages use the same command with the -e flag as follows.  Same instructions as above apply.

        ./target/release/packetcrypt ann -e http://pool.pktpool.io http://pool.pkt.world http://pool.srizbi.com http://pool.pkteer.com http://pktco.in --paymentaddr       pkt1q4rwkug8yl8k59h6kp5w6k3fqeug97rdfj682g7




