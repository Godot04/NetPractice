# NetPractice

This project was completed as part of the 42 curriculum.

NetPractice is a practical introduction to computer networking. Instead of memorizing theory only, each level gives a broken network topology and asks you to make communication work again.

## Project purpose

The goal of NetPractice is to build strong fundamentals in:

- IPv4 addressing
- subnet masks and CIDR notation
- network range and host range calculation
- default gateways
- static routing
- multi-subnet communication through routers

In short: understand why packets do or do not reach their destination, then fix the configuration.

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
- README.md - project documentation

## Running locally

1. Open net_practice/index.html in a browser.
2. Pick a level.
3. Fix the editable fields (IP, mask, routes, gateways).
4. Verify the reachability goals in the simulator.

Note: the subject mentions running through a helper script in some setups, but this repository currently uses the browser entry point above.

## Level-by-level purpose

### Level 1

Focus: basic host-to-host addressing in isolated segments.

What this level trains:

- reading an IP pattern
- assigning a valid address in the expected subnet
- avoiding invalid octet values

### Level 2

Focus: matching hosts inside one subnet with the correct mask.

What this level trains:

- identifying whether two hosts are in the same network
- selecting a mask that allows required communication
- validating host addresses against network and broadcast boundaries

### Level 3

Focus: subnet mask impact on LAN communication through a switch.

What this level trains:

- why L2 connectivity is not enough without consistent L3 configuration
- how mask mismatch breaks host reachability

### Level 4

Focus: first router-based segmentation.

What this level trains:

- assigning router interface addresses correctly
- understanding that each router interface belongs to a different subnet
- checking host-router subnet consistency

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
- distinction between local route knowledge and internet-facing paths
- designing minimal routing entries for complete reachability

### Level 7

Focus: communication across multiple router links.

What this level trains:

- coordinating host and router routes together
- keeping point-to-point and LAN masks coherent
- avoiding asymmetric routing paths

### Level 8

Focus: route precision in a multi-router topology.

What this level trains:

- adding specific routes toward remote subnets
- selecting the correct next hop
- preventing route conflicts between directly connected and remote networks

### Level 9

Focus: larger topology with several networks and route entries.

What this level trains:

- organizing routing logic for multiple destinations
- balancing default routes and more specific static routes
- troubleshooting complex reachability failures step by step

### Level 10

Focus: final integration challenge.

What this level trains:

- end-to-end reasoning from host to internet and between remote LANs
- mixed mask handling across many interfaces
- complete static routing strategy in a realistic mini-infrastructure

## What I learned

After finishing all exercises, I improved in:

- converting quickly between dotted masks and CIDR prefixes
- computing network, usable host range, and broadcast without guesswork
- choosing correct default gateways based on topology
- writing static routes with proper destination and next-hop logic
- debugging failures methodically: interface first, subnet second, route third

I also learned a practical mindset: do not change random values, always validate each change against packet path logic.

## Subject and evaluation notes

Based on the subject, evaluation includes solving random levels in a limited time during defense, so understanding the method is more important than memorizing values.

This README is intentionally focused on concepts and workflow rather than publishing per-level answer values.

## Resources

- 42 NetPractice subject PDF
- IPv4 and CIDR subnetting references
- Routing fundamentals (default route, longest-prefix match, next hop)

## AI usage

AI assistance was used for:

- proofreading and structuring documentation
- improving explanation clarity

All networking configurations and problem solving were completed manually in the NetPractice simulator.

## License

Project license is available in net_practice/License.
