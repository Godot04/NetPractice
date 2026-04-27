# NetPractice

This project was completed as part of the 42 curriculum.

NetPractice is a practical introduction to computer networking. Instead of memorizing theory only, each level gives an example of broken network and asks you to make users communication work again.

## Project purpose

The goal of NetPractice is to build strong fundamentals in:

- IPv4 addressing
- subnet masks
- network range and host range calculation
- default gateways
- static routing
- multi-subnet communication through routers

## How the project works

Each level contains machines, links, and communication objectives. Some values are correct and some are intentionally wrong.

Your task is to:

1. Analyze the topology.
2. Identify broken IP, mask, or route parameters.
3. Configure only what is editable.
4. Validate that all required hosts can reach each other.

The difficulty increases from simple local subnet checks to multi-router routing decisions.

## Repository structure

- net_practice/ - simulator files (HTML, CSS, JS, images)
- Tasks/ - exported solved configurations for levels 1 to 10

## Running locally

1. Open net_practice/index.html in a browser.
2. Pick a level.
3. Fix the editable fields (IP, mask, routes, gateways).
4. Verify correctness of that network. 

## Level-by-level purpose

### Level 1

Focus: basic host-to-host addressing in isolated segments.

What this level trains:

- reading an IP pattern
- assigning a valid address in the expected subnet
- avoiding an invalid IP range

### Level 2

Focus: matching hosts inside one subnet with the correct mask.

What this level trains:

- identifying whether two hosts are in the same network
- selecting a mask that allows required communication
- validating host addresses against network and broadcast boundaries

### Level 3

Focus: subnet mask impact on LAN communication through a switch.

What this level trains:

- How devices can be connected at the same switch but they still need matching IP settings (address, subnet mask, gateway) to communicate successfully.

### Level 4

Focus: first router-based segmentation.

What this level trains:

- assigning router interface addresses correctly
- understanding that each router interface belongs to a different subnet

### Level 5

Focus: introducing static routes and default gateways.

What this level trains:

- when to use a default route
- how hosts forward traffic outside their local subnet
- gateway selection based on directly connected router interface

### Level 6

Focus: routing from local network to an external network.

What this level trains:

- default route behavior on hosts and routers
- difference between local route knowledge and internet-facing paths
- Setting up the smallest possible routing table that still allows full communication across the whole network.

### Level 7

Focus: communication across multiple router links.

What this level trains:

- coordinating host and router routes together
- avoiding asymmetric routing paths

### Level 8

Focus: route precision in a multi-router topology.

What this level trains:

- adding specific routes toward remote subnets
- preventing route conflicts between directly connected and remote networks

### Level 9

Focus: working with a bigger network that has many subnets and multiple routing rules.

What this level trains:

- organizing routing logic for multiple destinations
- balancing default routes and more specific static routes
- finding and fixing difficult connection problems by checking the network one part at a time.

### Level 10

Focus: final integration challenge.

What this level trains:

- end-to-end reasoning from host to internet and between remote LANs
- mixed mask handling across many interfaces
- complete static routing strategy in a mini-infrastructure

## What I learned

After finishing all exercises I improved in:

- converting quickly between dotted masks and CIDR prefixes
- computing network, usable host range, and broadcast
- choosing correct default gateways based on topology
- debugging failures methodically: interface first, subnet second, route third
