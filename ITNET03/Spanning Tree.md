- Redundancy at OSI layers 1 and 2
- as businesses become increasingly dependent on the network, the availability becomes a concern
	- how does availability = redundancy?
		- By adding alternate network paths from adding equipment and cabling to eliminate a single point of failure
	- Multiple paths allow a single path to be disrupted

#### Issue with Layer 1 Redundancy: MAC Database instability
- Ethernet frames do not have TTL field like Layer 3 IP 
- inconsistent databases send to repeated switches
#### Issue with Layer 1 redundancy: Broadcast storms
- Cyclic graphs are unavoidable with redundant links this leads to braodcast storms from looping braodcast data


#### Spanning Tree algorithms
- Aims to eliminate repeated links from each node 
	- How does this help our redundancy code? 
- Phyisically, you may connect to multiple switches(redundancy) but spanning trees are deployed logically. To eliminate cyclic link

#### STP (Spanning Tree Operation as a Network Algorithm)
- STP creates a loop free topology by selecting a single root bridge to which all other switches determine the least costly path
- Redundant paths that can cause a loop are dynamically blocked
- STP sends ***bridge protocol data unit***frames to calculate the one logical path
- During failure, blocked links are unblocked to server the alternative path

1. Pick the root bridge
2. Calculate path costs to the root
3. Select Root Ports
4. Select Designated Ports
5. Select Non-Designated Blocked ports 

During STA and STP functions, switches use bridge protocol data units to share information about themselves and their connections 


