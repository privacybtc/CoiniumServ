# ![Screenshot](http://coinium.org/assets/images/logo/coinium-icon-48.png) CoiniumServ [![Build Status](https://travis-ci.org/CoiniumServ/CoiniumServ.svg?branch=develop)](https://travis-ci.org/CoiniumServ/CoiniumServ) [![Build status](https://ci.appveyor.com/api/projects/status/3x349ig9dt14943t)](https://ci.appveyor.com/project/raistlinthewiz/coiniumserv)
 
[CoiniumServ](https://github.com/CoiniumServ/CoiniumServ) is an high performance, extremely efficient, platform-agnostic, easy to setup pool server implementation. It features stratum and vanilla services, reward, payment, share processors, vardiff & ban managers, user-friendly embedded web-server & front-end and a full-stack API.

CoiniumServ was created to be used for [Coinium.org](http://www.coinium.org) mining pool network at first hand. You can check [some of pools](https://github.com/CoiniumServ/CoiniumServ/wiki/Pools) of the pools running CoiniumServ.

* Official pools: [coinium.org](http://www.coinium.org)

![CoiniumServ running over mono & ubuntu](http://i.imgur.com/izIB5nq.png)

### Support

Start by reading our [FAQ](https://github.com/CoiniumServ/CoiniumServ/wiki/FAQ) and [wiki](https://github.com/CoiniumServ/CoiniumServ/wiki/). If you need further help, join us over our user-support channel [#coiniumserv@freenode](http://webchat.freenode.net/?channels=%23coiniumserv&prompt=1&uio=OT10cnVlde).

You can also use our [issues](https://github.com/CoiniumServ/CoiniumServ/issues) page to report bugs.

* Official site: [coiniumserv.com](http://www.coiniumserv.com)
* [Paid support & consulting options](https://github.com/CoiniumServ/CoiniumServ#consulting)
* [Support forums](http://forum.coinium.org/forum/19-support/)
* IRC (**irc.freenode.net**):
  - **#coiniumserv** [user support](http://webchat.freenode.net/?channels=%23coiniumserv&prompt=1&uio=OT10cnVlde)
  - **#coiniumserv-dev** [dev talk](http://webchat.freenode.net/?channels=%23coiniumserv-dev&prompt=1&uio=OT10cnVlde)
  - **#coinium** [official pools](http://webchat.freenode.net/?channels=%23coinium&prompt=1&uio=OT10cnVlde)
* [Twitter](http://twitter.com/coinium)
* [Bitcointalk.org](https://bitcointalk.org/index.php?topic=604476.0)
* [Bitcoin wiki](https://en.bitcoin.it/wiki/CoiniumServ)

### Donation

You can contribute the development of the project by donating; 

* BTC: `18qqrtR4xHujLKf9oqiCsjmwmH5vGpch4D`
* LTC: `LMXfRb3w8cMUBfqZb6RUkFTPaT6vbRozPa`
* DOGE: `DM8FW8REMHj3P4xtcMWDn33ccjikCWJnQr`
* RDD: `Rb9kcLs96VDHTmiXVjcWC2RBsfCJ73UQyr`

If you would like to automatically donate a percentage of your pool's earning to support the project, check the [donation setup](https://github.com/CoiniumServ/CoiniumServ/wiki/Donation) guide.

###### Donors

Here is a list of our generous donors that keep the project ongoing;

* [reddapi.com](https://www.reddapi.com)

###### Bounties

BountySource integration available over [here](https://www.bountysource.com/trackers/401667-coiniumserv). You can set bounties and solve them.

[![Bountysource](https://api.bountysource.com/badge/team?team_id=760&style=bounties_received)](https://www.bountysource.com/teams/coinium/issues?utm_source=Coinium&utm_medium=shield&utm_campaign=TEAM_BADGE_1)

###### Tips

You can send tips and furher support the project or get tips for contributing by commiting.

[![tip for next commit](http://tip4commit.com/projects/760.svg)](http://tip4commit.com/projects/760)

### Status

[v0.1.2 alpha](https://github.com/CoiniumServ/CoiniumServ/releases/tag/v0.1.2-alpha) released

### Features

###### Platform Agnostic
Can run on these platforms;
* Linux/Unix over [mono](http://www.mono-project.com/).
* MacOS over [mono](http://www.mono-project.com/).
* Windows over [.Net](http://www.microsoft.com/net).

###### Multiplexed Structure
* Multiple pools & ports.
* Multiple coin daemon connection support.
* Multiple storage layers.

###### Functionality
* Stratum server (over TCP sockets).
* Stratum show_message support (MOTD & messages).
* Vanilla server (getwork over http server). [experimental]
* Daemon RPC interface.
* Storage layers support
* Block template / job managment.
* Generation transaction builder.
* Share processor.
* Payment processor.
* Proof of Work (PoW) and Proof of Stake (PoS) support.
* Transaction messages support.
* Vardiff support.
* Ban manager support that can handles miners flooding with invalid shares.
* Embedded web-server & front-end
* Full-stack API

###### Hashing Algorithms

_Working_
* ✓ __Scrypt__ 

_Needs Testing_

* ✓ __SHA256__ 
* ✓ __Blake__
* ✓ __Fugue__
* ✓ __Groestl__
* ✓ __Keccak__ 
* ✓ __SHAvite3__
* ✓ __Skein__ 
* ✓ __multi-algos: X11, X13, X14, X15, X17__

_Under Development_

* ✓ __Scrypt-Jane__ 
* ✓ __Scrypt-N__ 
* ✓ __Scrypt-OG__ 
* ✓ __Quark__ 
* ✓ __NIST5__
* ✓ __Qubit__
* ✓ __Hefty1__
 
###### Persistance & Storage Layers

CoiniumServ supports storage layer interfaces that you can extend to implement your own persistance logic. By default, it supports two layers; a high performance hybrid layer and mpos compatibility layer.

* __Hybrid Layer__: a custom hybrid layer that utilizes redis + mysql together that is carefully designed for high performance persistance support.
* __MPOS Layer__: a compatibility layer based on mysql that supports MPOS whenever you want payments to be handled by MPOS.

###### Development Model
* Strictly [follows](https://github.com/CoiniumServ/CoiniumServ/tree/develop/src/Tests) the [Test Driven Development](http://en.wikipedia.org/wiki/Test-driven_development) model. We have implemented extensive [tests](https://github.com/CoiniumServ/CoiniumServ/tree/develop/src/Tests) for all important functionality and never merge in code that breaks tests and stuff. Yet again, when a new functionality is introduced we also expect proper tests to be implemented within the PR. In simple words, most probably you won't notice any functionality-breaking changes within the repository.
* A strict ruleset for the [Development Model](https://github.com/CoiniumServ/CoiniumServ/wiki/Development-Model). You can follow our bleeding-edge [Develop](https://github.com/CoiniumServ/CoiniumServ) branch or stay with-in the stable [Master](https://github.com/CoiniumServ/CoiniumServ/tree/master) branch.
   

### Getting Started

Make sure you check our [Getting Started](https://github.com/CoiniumServ/CoiniumServ/wiki/Getting-Started) guide for installation instructions for *nix and Windows.

For Ubuntu, you can simply use our installer script;

```
wget -O - https://raw.githubusercontent.com/CoiniumServ/CoiniumServ/develop/contrib/installers/ubuntu.sh | bash
```

### Documentation

* [Wiki](https://github.com/CoiniumServ/CoiniumServ/wiki/)
* [FAQ](https://github.com/CoiniumServ/CoiniumServ/wiki/FAQ)
* [Master Plan](https://github.com/CoiniumServ/CoiniumServ/wiki/Master-Plan)

### Contributing

Start reading by these;

* [Developer's Guide](https://github.com/CoiniumServ/CoiniumServ/wiki/Developer's-Guide)
* [Technical Documentation](https://github.com/CoiniumServ/CoiniumServ/wiki/Technical-Documentation)

### Consulting

Additional to free [support](https://github.com/CoiniumServ/CoiniumServ#support) methods, we offer paid remote support & consulting services for whom would like to get professional support. Contact us over [here](http://blog.coinium.org/coiniumserv/consulting/) and we will get back to you to discuss your needs.

### License

Copyright (C) 2013 - 2014, CoiniumServ Project - http://www.coinium.org - 
http://www.coiniumserv.com - https://github.com/CoiniumServ/CoiniumServ

This software is dual-licensed: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

For the terms of this license, see [licenses/gpl_v3.txt](https://github.com/CoiniumServ/CoiniumServ/blob/develop/licenses/gpl_v3.txt).

Alternatively, you can license this software under a commercial
license or white-label it as set out in [licenses/commercial.md](https://github.com/CoiniumServ/CoiniumServ/blob/develop/licenses/commercial.md).

