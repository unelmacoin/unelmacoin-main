#### Installation instructions for running UnelmaCoin in Ubuntu/Linux
(Have been tested on Ubuntu 18.04 LTS)

First we will install Build dependencies:

Build requirements:

`sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git`


On at least Ubuntu 14.04+ and Debian 7+ there are generic names for the individual boost development packages, so the following can be used to only install necessary parts of boost:

`sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev`

If that doesn't work, you can install all boost development packages with:

`sudo apt-get install libboost-all-dev`

BerkeleyDB is required for the wallet. db4.8 packages are available here. You can add the repository and install using the following commands:

`sudo apt install software-properties-common`</br>
`sudo add-apt-repository ppa:bitcoin/bitcoin`</br>
`sudo apt-get update`</br>
`sudo apt-get install libdb4.8-dev libdb4.8++-dev`</br>

Optional:

`sudo apt-get install libminiupnpc-dev (see --with-miniupnpc and --enable-upnp-default)`

ZMQ dependencies:

`sudo apt-get install libzmq3-dev (provides ZMQ API 4.x)`

Now lets start:

Download unelmacoin github source:


`git clone https://github.com/unelmacoin/unelmacoin-main`

Now we are going to compile the Client:

`chmod a+x+w -R unelmacoin-main/` </br>
`cd unelmacoin-main` </br>
`./autogen.sh` </br>
`sudo apt-get remove openssl` </br>
`sudo apt-get install libcurl3` </br>
`sudo apt-get install openssl1.0-dev` </br>
`./configure`</br>
`make`</br>
`make install`</br>

Now lets run the unelmacoin daemon:

`unelmacoind &`
press enter

You should see the unelmacoind daemon up and running in Ubuntu distribution. 
