#### Installation instructions for running UnelmaCoin in Ubuntu/Linux

First we will install Build dependencies:

Build requirements:

`sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git`


On at least Ubuntu 14.04+ and Debian 7+ there are generic names for the individual boost development packages, so the following can be used to only install necessary parts of boost:

`sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev`

If that doesn't work, you can install all boost development packages with:

`sudo apt-get install libboost-all-dev`

BerkeleyDB is required for the wallet. db4.8 packages are available here. You can add the repository and install using the following commands:

`sudo add-apt-repository ppa:bitcoin/bitcoin`
`sudo apt-get update`
`sudo apt-get install libdb4.8-dev libdb4.8++-dev`

Optional:

`sudo apt-get install libminiupnpc-dev (see --with-miniupnpc and --enable-upnp-default)`

ZMQ dependencies:

`sudo apt-get install libzmq3-dev (provides ZMQ API 4.x)`

Now lets start:

Download unelmacoin github source:


`git clone https://github.com/unelmacoin/unelmacoin-main`

Now we are going to compile the Client:

`chmod a+x+w -R unelmacoin-main/`
`cd unelmacoin-main`
`./autogen.sh`
`./configure`
`make`
`make install`

Now lets run the unelmacoin daemon:

`unelmacoind &`
press enter

You should see the unelmacoind daemon up and running in Ubuntu distro
