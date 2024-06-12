# Description

Tests SMB ascii directory name instead of unicode with two rules.
One rule has to be avoided. The other one is well written.

# PCAP

The pcap comes from running Linux client smbclient against a Windows 2019 Server (with a shared folder public without needed authentication)

Needs a Proxy that sends the connexion smb packet without unicode flag.

Command is
`smbclient //localhost/C$/ -U username%password -m NT1`
Than in the smbclient shell :
`cd Windows\System32`
`put file` where file can be any file
