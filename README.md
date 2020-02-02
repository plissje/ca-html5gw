# ca-html5gw
Script to automate the setup of CyberArk's HTML5 Web Gateway.

<p align="center">
    <img src="https://cdn.rawgit.com/strick-j/ca-html5gw/94fa5f69/examples/html5install.svg">
</p>

# Installation
Intended for installation on an updated minimal CentOS 7 Server. General install instructions:
1. Clone or download the git repository
2. Copy the necessary Cyber Ark PSMGW rpm file into the local git repository
3. Update passwords within the script to desired password, do not update the password for the Java Keystore "changeit" unless you have changed this password from the default.
4. Run the setup script as a user with admin rights (e.g. "sudo ./html5gw-setup.sh")
5. The tomcat certificate is exported from the /opt/secrets/keystore and will be located in the directory the script is ran from with the name "tomcat.cer". You can import this on client workstations to trust the connection to the HTML5GW.

# Notes / Prerequisites
This is a modified version of the original script which needs an input for both the keystore passwords and the certificate details (The installer uses a self-siged certificate, but the keystore has a SAN configuration which simplifies the process of creating a CSR)
