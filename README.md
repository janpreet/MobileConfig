# MobileConfig

Apple profile to install [Open DNS Family Shield](https://www.opendns.com/setupguide/#familyshield) DNS over HTTPS. Traffic will be routed to OpenDNS family-shield DoH endpoint. [Link to official page](https://support.opendns.com/hc/en-us/articles/360038086532-Using-DNS-over-HTTPS-DoH-with-OpenDNS)
|Hostname	| Description |
| :---: | :---: | 
|doh.familyshield.opendns.com| A DoH frontend to our FamilyShield DNS service, pre-configured to block adult content, as provided on 208.67.222.123 and 208.67.220.123|

## Installation
1. Download the profile from this page or [this link](https://raw.githubusercontent.com/janpreet/MobileConfig/main/familyShield.mobileconfig).
2. Go to Settings -> General -> VPN & Device Management -> Downloaded Profile (OpenDNS FamilyShield) -> Install.

## Uninstallation
1. Go to Settings -> General -> VPN, DNS & Device Management -> Configuration Profile (OpenDNS FamilyShield) -> Remove Profile.
