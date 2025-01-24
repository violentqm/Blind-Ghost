# [Blind-Ghost]
# The Setup
run the script on any infected machine/zombie

The zombie starts pretending to be the "answer machine" for all .local name requests (like \\wpad or \\fileserver).

# exploit?
When any other device on the network tries to access a .local name (e.g., by mistyping a share name or during a network scan), the zombie jumps in

This tricks the victim into connecting to the zombie instead of the real server.

# the infection
The zombie then uses a sneaky trick with the victim’s browser:

It injects a bit of JavaScript into every webpage the victim visits.

The JavaScript forces the victim to download and run a powershell script


# Why It Works
LLMNR/NBT-NS: Windows uses these protocols to find devices on the network, and they’re enabled by default.

HTTP Coercion: Browsers automatically download and run files from trusted sources (like the zombie’s fake server).

No Credentials Needed: The script doesn’t need passwords or exploits—it just abuses how Windows and browsers work.

# whats special
Fileless: No files are written to disk on the victim’s machine.

Blind: It works without knowing the IPs or names of other devices.

Native Tools: It uses only built-in Windows features (PowerShell, LLMNR, HTTP).
