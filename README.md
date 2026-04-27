# NetPractice

This project was completed as part of the 42 curriculum.

NetPractice is a browser-based networking lab where each level gives a broken topology and a set of communication goals. The objective is to fix IP addressing, subnet masks, and routing tables so every required host can reach the others.

All exercises in this repository are solved.

## Repository structure

- `net_practice/` - web simulator files (HTML/CSS/JS + assets)
- `Tasks/` - solved values per level (`level1.json` ... `level10.json`)

## What I learned

- IPv4 addressing and subnetting (`/25`, `/26`, `/27`, `/30`, etc.)
- How to detect wrong host/network/broadcast assignments
- Static routing and default gateway design
- Multi-router path construction and route specificity
- Troubleshooting end-to-end connectivity in segmented networks

## How to run locally

1. Open `net_practice/index.html` in a browser.
2. Select a level.
3. Apply IP/mask/route fixes.
4. Validate reachability goals in the simulator.

## Exercise solutions

Below is the final answer key based on the solved files in `Tasks/`.

### Level 1

Interfaces:

- `A1.ip = 104.94.23.13`
- `D1.ip = 211.191.170.76`

### Level 2

Interfaces:

- `A1.ip = 192.168.150.221`
- `B1.mask = 255.255.255.224`
- `C1.ip = 192.168.150.1`
- `D1.ip = 192.168.150.2`

### Level 3

Interfaces:

- `A1.mask = 255.255.255.128`
- `B1.ip = 104.198.29.124`
- `B1.mask = 255.255.255.128`
- `C1.ip = 104.198.29.126`

### Level 4

Interfaces:

- `A1.mask = 255.255.255.128`
- `B1.ip = 119.177.113.131`
- `B1.mask = 255.255.255.128`
- `R1.ip = 119.177.113.130`
- `R1.mask = /25`

### Level 5

Interfaces:

- `A1.ip = 21.220.165.125`
- `A1.mask = /25`
- `B1.ip = 138.64.139.253`
- `B1.mask = /18`

Routes:

- `Ar1.route = default`
- `Ar1.gate = 21.220.165.126`
- `Br1.gate = 138.64.139.254`

### Level 6

Interfaces:

- `A1.mask = /25`
- `R1.ip = 21.51.23.226`

Routes:

- `Ar1.route = default`
- `Ar1.gate = 21.51.23.226`
- `Rr1.route = default`
- `Ir1.route = 21.51.23.128/25`

### Level 7

Interfaces:

- `A1.ip = 101.198.14.2`
- `A1.mask = /26`
- `C1.ip = 101.198.14.116`
- `C1.mask = /26`
- `R11.mask = /26`
- `R12.mask = /26`
- `R21.ip = 101.198.14.253`
- `R21.mask = /26`
- `R22.ip = 101.198.14.117`
- `R22.mask = /26`

Routes:

- `Ar1.route = default`
- `Ar1.gate = 101.198.14.1`
- `Cr1.route = default`
- `Cr1.gate = 101.198.14.117`
- `R1r1.route = default`
- `R1r1.gate = 101.198.14.253`
- `R2r1.route = default`
- `R2r1.gate = 101.198.14.254`

### Level 8

Interfaces:

- `C1.ip = 131.62.36.19`
- `C1.mask = /28`
- `D1.ip = 131.62.36.2`
- `R13.ip = 131.62.36.62`
- `R13.mask = /28`
- `R21.ip = 131.62.36.61`
- `R21.mask = /28`
- `R22.ip = 131.62.36.18`
- `R22.mask = /28`
- `R23.ip = 131.62.36.1`
- `R23.mask = /28`

Routes:

- `Cr1.route = default`
- `Cr1.gate = 131.62.36.18`
- `Dr1.route = default`
- `Dr1.gate = 131.62.36.1`
- `R1r2.route = 131.62.36.0/26`
- `R1r2.gate = 131.62.36.61`
- `R2r1.route = default`
- `Ir1.gate = 163.74.250.12`

### Level 9

Interfaces:

- `A1.ip = 1.2.3.3`
- `A1.mask = /25`
- `B1.ip = 1.2.3.2`
- `B1.mask = /25`
- `C1.ip = 6.7.8.2`
- `C1.mask = /24`
- `D1.ip = 58.85.11.129`
- `D1.mask = /18`
- `R11.ip = 1.2.3.1`
- `R13.ip = 5.4.3.2`
- `R13.mask = 255.255.255.252`
- `R21.ip = 5.4.3.1`
- `R22.ip = 6.7.8.1`
- `R22.mask = /24`
- `R23.ip = 58.85.11.128`

Routes:

- `Ar1.route = default`
- `Ar1.gate = 1.2.3.1`
- `Br1.route = default`
- `Br1.gate = 1.2.3.1`
- `Cr1.gate = 6.7.8.1`
- `Dr1.route = default`
- `R1r1.route = 58.85.11.0/18`
- `R1r1.gate = 5.4.3.1`
- `R1r2.route = 6.7.8.0/24`
- `R1r2.gate = 5.4.3.1`
- `R2r1.gate = 5.4.3.2`
- `Ir1.route = 1.2.3.0/25`
- `Ir2.route = 58.85.11.0/18`
- `Ir3.route = 6.7.8.0/24`

### Level 10

Interfaces:

- `H11.mask = /25`
- `H21.ip = 136.197.8.3`
- `H21.mask = /25`
- `H31.ip = 136.197.8.194`
- `H31.mask = /27`
- `R13.mask = /30`
- `R22.ip = 136.197.8.193`
- `R22.mask = /27`
- `R23.ip = 136.197.8.129`
- `R23.mask = /26`

Routes:

- `H3r1.gate = 136.197.8.193`
- `R1r1.route = default`
- `Ir1.route = 136.197.8.0/0`

## Notes

- Route names (`Ar1`, `R1r1`, etc.) and interface IDs (`A1`, `R22`, etc.) are the simulator identifiers.
- CIDR and dotted masks are both used by NetPractice depending on the level.
- The solved values are taken directly from the JSON files in `Tasks/`.

## License

Project license is available in `net_practice/License`.
