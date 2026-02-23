*This project has been created as part of the 42 curriculum by [wnid-hsa].*

# NetPractice

## Description

NetPractice is a practical networking exercise project from the 42 curriculum. Its goal is to build a solid understanding of TCP/IP networking by solving a series of progressively challenging network configuration puzzles through an interactive training interface.

Each level presents a broken network diagram, and the task is to correctly configure IP addresses, subnet masks, and routing rules so that all hosts can communicate with one another. By completing all 10 levels, you develop hands-on intuition for how real networks are designed and debugged.

Topics covered include:
- TCP/IP addressing (IPv4)
- Subnet masks and CIDR notation
- Network and broadcast addresses
- Default gateways
- Routers and switches (layer 2 vs layer 3 forwarding)
- Routing tables and packet forwarding logic
- The OSI model layers (with focus on Network and Data Link layers)

---

## Instructions

### Running the Training Interface

A `run.sh` script is provided to launch the NetPractice web interface locally:

```bash
bash run.sh
```

Then open your browser and navigate to the address shown in the terminal (typically `http://localhost:port`). Log in using your 42 login to load your session.

### Solving Levels

- Work through all **10 levels** in order.
- Each level requires you to fill in missing network configuration values (IP addresses, masks, routes) until the network diagram turns green and all connections are valid.
- Use the **Check** button to validate your configuration for each level.

### Exporting Configurations

Once a level is successfully completed:

1. Click the **Export** button in the interface.
2. Save the generated `.json` configuration file.
3. Rename it according to the level (e.g., `level1.json`, `level2.json`, ..., `level10.json`).

### Submission Requirements

All **10 exported configuration files** (one per level) must be placed at the **root of your Git repository** before submitting:

```
/
├── level1.json
├── level2.json
├── level3.json
├── level4.json
├── level5.json
├── level6.json
├── level7.json
├── level8.json
├── level9.json
├── level10.json
└── README.md
```

Push all files to your repository before the submission deadline. No source code compilation is required : only the exported JSON files and this README are needed.

---

## Resources

### Networking Documentation & References

The following YouTube videos were used to build understanding of the networking concepts required for this project:

- [شرح ال IP Address خطوة بخطوة والنظام الثنائي](https://youtu.be/uQbr9d1C9sA)
- [Professional Subnetting Explained - Class A Examples - Part 3](https://youtu.be/azbSw2TKTuI)
- [Subnetting explained from the other - examples of Class C and Class B - Part 2](https://youtu.be/ClXJcwg_JCk)
- [شرح مفصل لل IP Address وال Subnet Mask, الفرق بين Public IP Vs Private IP](https://youtu.be/Nnv36wG_iCI)
- [Explaining TCP/IP in detail and the difference between it and the OSI Model](https://youtu.be/MfNheIcKCmM)
- [شرح ال OSI Model وال 7 مراحل شرح مبسط بالعربي في 20 دقيقة فقط](https://youtu.be/61kRxdZ5p-o)

### Networking Concepts Studied

The following concepts were studied and applied throughout this project:

- **TCP/IP Addressing**: Understanding IPv4 address structure (network vs host portion), classes, and private ranges.
- **Subnet Masks** : Using masks (e.g., `255.255.255.0` / `/24`) to determine which addresses belong to the same network.
- **CIDR Notation** : Expressing subnet masks in prefix-length format (e.g., `/26`, `/28`).
- **Network & Broadcast Addresses** : Identifying the first (network) and last (broadcast) addresses in a subnet, which cannot be assigned to hosts.
- **Default Gateways** : Configuring the router interface address that a host sends packets to when the destination is outside its local subnet.
- **Routers** : Devices operating at OSI Layer 3 that forward packets between different networks using routing tables.
- **Switches** : Devices operating at OSI Layer 2 that forward frames within the same network using MAC addresses.
- **Routing Tables** : Understanding how a router or host decides where to forward a packet based on destination IP and configured routes.
- **OSI Model Layers** : Particularly Layer 1 (Physical), Layer 2 (Data Link / switching), and Layer 3 (Network / routing).

### AI Usage

AI (Claude by Anthropic) was used during this project for the following tasks:

- **Concept clarification** : Asking questions about subnetting rules, CIDR notation, and how routing tables are evaluated when multiple routes could match.
- **Verification of reasoning** : Double-checking subnet calculations (e.g., confirming valid host ranges for a given mask) before applying them in the interface.

AI was **not** used to directly solve any of the 10 NetPractice levels. All network configurations were worked out manually through the training interface.
