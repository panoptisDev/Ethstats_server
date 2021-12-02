# Ethstats_server
Ethereum Network Stats with POA and POW support
 
This is a visual interface for tracking proof-of-work ("mainnet") and proof-of-authority ("testnet") network status. It uses WebSockets to receive stats from running nodes and output them through an angular interface. It is the front-end implementation for ethstats-client.

Panoptis Proof-of-Authority


Demo: https://stats.goerli.net/

Demo: https://kotti.goerli.net/



Prerequisite

node
npm


Installation
Make sure you have node.js and npm installed.
Clone the repository and install the dependencies:
git clone https://github.com/goerli/ethstats-server
cd ethstats-server
npm install
sudo npm install -g grunt-cli

Build
In order to build the static files you have to run grunt tasks which will generate dist directories containing the js and css files, fonts and images.
grunt poa
To build the static files for a network other than Ethereum copy and change src/js/defaultConfig.js and run the following command.
grunt poa --configPath="src/js/someOtherConfig.js"

Run
Start a node process and pass the websocket secret to it.
WS_SECRET="asdf" npm start
Find the interface at http://localhost:3000

Proof-of-Work (Legacy)


Demo: https://mordor.dash.fault.dev/


Same as above, just run the pow build task in Grunt.
grunt pow
WS_SECRET="asdf" npm start
