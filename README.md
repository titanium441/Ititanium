

### Coin Information

Algorithm                  : Scrypt

Type                       : PoW/PoS

Coin name                 : ITITANIUMCOIN

Coin abbreviation         :  ITC

Address letter            : T

RPC port                   : 27040

P2P port                   : 27039

Block reward           : 75 coins

Total coin supply     : 38414634 coins

Premine percent     : 18%

Premine amount     : 6914634 coins

PoS percentage      : 100% per year

Last PoW block       : 10000

Coinbase maturity : 20 blocks

Target spacing       : 64 seconds

Target timespan    : 1 block

Transaction confirmations : 3 blocks


ITITANIUMCOIN development tree

ITITANIUMCOIN is a PoS-based cryptocurrency.

Development process
===========================

Developers work in their own trees, then submit pull requests when
they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a
good thing.  Developers should expect to rework and resubmit patches
if they don't match the project's coding conventions (see coding.txt)
or are controversial.

The master branch is regularly built and tested, but is not guaranteed
to be completely stable. Tags are regularly created to indicate new
stable release versions of ITITANIUMCOIN.

Feature branches are created when there are major new features being
worked on by several people.

From time to time a pull request will become outdated. If this occurs, and
the pull is no longer automatically mergeable; a comment on the pull will
be used to issue a warning of closure. The pull will be closed 15 days
after the warning if action is not taken by the author. Pull requests closed
in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after
15 days from their last activity. Issues closed in this manner will be 
labeled 'stale'.


### Website : https://www.ititaniumcoin.com

In Your ititaniumcoin.conf file just at this line

- addnode=122.175.85.234
- addnode=128.199.207.95
- addnode=159.89.143.160
- addnode=165.227.32.10
- addnode=183.82.141.42
- addnode=188.166.175.218
- addnode=188.226.164.41
- addnode=37.97.242.80

### Blockchain explorer :

https://chainz.cryptoid.info/itc/

### Forum Announcement :

https://bitcointalk.org/index.php?topic=2534169.msg25837502#msg25837502

### Install Linux Dependncies :

General :

sudo apt-get install git build-essential openssl libminiupnpc-dev build-essential openssl libminiupnpc-dev automake libtool libprotobuf-dev qrencode autoconf-tools cmake libevent-dev libcurl4-openssl-dev sudo apt-get install libqt4-dev qt4-dev-tools sudo apt-get install libqt5-dev qt5-dev-tools qttools5-dev-tools qt5-default libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools sudo apt-get install software-properties-common sudo add-apt-repository ppa:bitcoin/bitcoin sudo apt-get update sudo apt-get install libdb4.8-dev libdb4.8++-dev Latest version of LibBoost: sudo apt-get install libboost++-dev libboost-all-dev libssl-dev libdb++-dev instructions for Linux compile:

git clone https://github.com/ititaniumcoin/ititaniumcoin cd ititaniumcoin sudo chmod +777 * ./autogen.sh ./configure make

Example regular inernet Users ititaniumcoin.conf

rpcuser=ITITANIUMCOINusername rpcpassword=ITITANIUMCOINuserpass

Development tips and tricks

### Development Tips and Tricks

compiling for debugging

Run configure with the --enable-debug option, then make. Or run configure with CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need. debug.log

If the code is behaving strangely, take a look in the debug.log file in the data directory; error and debugging messages are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt to see it.

testnet and regtest modes

Run with the -testnet option to run with "play batas" on the test network, if you are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option. In regression test mode, blocks can be created on-demand; see qa/rpc-tests/ for tests that run in -regtest mode.

### DEBUG_LOCKORDER

Bata Core is a multithreaded application, and deadlocks or other multithreading bugs can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of which locks are held, and adds warnings to the debug.log file if inconsistencies are detected.

