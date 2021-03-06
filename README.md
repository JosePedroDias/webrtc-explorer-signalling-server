About this fork:

There seemed to be far too many dependencies being fetched with the regular `package.json`.  
Simplified it a lot so it works with no frills.

To install do:

    [sudo] npm install

To run:

	node ./src/index.js
	
To change the parameters of the network edit the config file.


-------


webrtc-explorer Signalling Server
==============================

> The `webrtc-explorer Signaling Server` implements the spec defined for the `webrtc-explorer` browser based DHT work properly, please refer to the [webrtc-explorer docs](https://github.com/diasdavid/webrtc-explorer) for instructions. 

# Badgers

[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/diasdavid/webrtc-ring?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) 
[![Dependency Status](https://david-dm.org/diasdavid/webrtc-signalling-server.svg)](https://david-dm.org/diasdavid/webrtc-ring-signalling-server)

[![](https://cldup.com/pgZbzoshyV-3000x3000.png)](http://www.gsd.inesc-id.pt/)

# Spec

## Events listented by the server

- `s-register` - register a node on the DHT, assign him uuid and inform that Node of his Id through `c-registered`

- `s-send-offer` - forward signaling data from one client that wants to connect to another client

- `s-offer-accepted` - forward response signaling data

## Events emitted by the server

- `c-finger-update` - let a client know that he should update one of his fingers
- `c-predecessor` - let a client know of his predecessorId

- `c-offer-accepted` - forward response signaling data

- `c-accept-offer` - Ask a client to accept an offer from another client 

- `c-registered` - tell a client he is registered and what is their Id

