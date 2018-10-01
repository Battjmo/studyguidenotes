# REST

REpresentational State Transfer

design principles for making networks scalable and flexible

coined by Fielding in 2000 in dissertation Architectural Styles and the Design of Network-based Software Architectures

## fielding constraints

1. client server: network is made up of thet two. server has resourdces, client wnts resources

2. stateless: client and server don't need to know each other's state

3. uniform interface: common language between the two so each part can be swapped or modded without evewrything breaking.

4 subparts

  1. ident of resources: every resources needs a stable identity, even when changed. URI's
  2. manipulate resources thru representations: client sends JSON representation of changes they'd like to make to server, 
  which makes the changes
  3. self-descriptive messages: message contains everything needed to comprehend it
  4. server only sends hypermedia(HTML) to client

4. caching: server message tells client whether it should save the data or not to speed things up in the future

5. layers systems: systems have layers, and each layer can only talk to the next one

6. code on demand: optional, server can send executable code to client

