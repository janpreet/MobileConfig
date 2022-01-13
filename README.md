# MobileConfig

Apple profile to install [Open DNS Family Shield](https://www.opendns.com/setupguide/#familyshield) DNS over HTTPS. All traffic, regardless of access-point (WiFi or Cellular), will be encrypted and routed to OpenDNS family-shield DoH endpoint. [Link to official page](https://support.opendns.com/hc/en-us/articles/360038086532-Using-DNS-over-HTTPS-DoH-with-OpenDNS)
|Hostname	| Description |
| :---: | :---: | 
|doh.familyshield.opendns.com| A DoH frontend to our FamilyShield DNS service, pre-configured to block adult content, as provided on 208.67.222.123 and 208.67.220.123|

## Installation
1. Download the profile from this page or [this link](https://raw.githubusercontent.com/janpreet/MobileConfig/main/familyShield.mobileconfig).
2. Go to Settings -> General -> VPN & Device Management -> Downloaded Profile (OpenDNS FamilyShield) -> Install.

## Uninstallation
1. Go to Settings -> General -> VPN, DNS & Device Management -> Configuration Profile (OpenDNS FamilyShield) -> Remove Profile.

## Profile content
Use Apple configurator to unsign the profile, and open it with a text editor of your choice, if you'd like to see the code. Here's what's inside-
```mobileconfig
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>PayloadContent</key>
	<array>
		<dict>
			<key>DNSSettings</key>
			<dict>
				<key>DNSProtocol</key>
				<string>HTTPS</string>
				<key>ServerURL</key>
				<string>https://doh.familyshield.opendns.com/dns-query</string>
			</dict>
			<key>PayloadDescription</key>
			<string>OpenDNS FamilyShield over HTTPS</string>
			<key>PayloadDisplayName</key>
			<string>OpenDNS FamilyShield</string>
			<key>PayloadIdentifier</key>
			<string>com.apple.dnsSettings.managed.650b10a7-6355-4576-a549-d3975a1e29f1</string>
			<key>PayloadType</key>
			<string>com.apple.dnsSettings.managed</string>
			<key>PayloadUUID</key>
			<string>650b10a7-6355-4576-a549-d3975a1e29f1</string>
			<key>PayloadVersion</key>
			<integer>1</integer>
			<key>ProhibitDisablement</key>
			<false/>
		</dict>
	</array>
	<key>PayloadDescription</key>
	<string>OpenDNS FamilyShield over HTTPS</string>
	<key>PayloadDisplayName</key>
	<string>OpenDNS FamilyShield</string>
	<key>PayloadIdentifier</key>
	<string>familyShield</string>
	<key>PayloadOrganization</key>
	<string>Janpreet Singh</string>
	<key>PayloadRemovalDisallowed</key>
	<false/>
	<key>PayloadType</key>
	<string>Configuration</string>
	<key>PayloadUUID</key>
	<string>79CAC10D-F6BF-4372-9C13-B0AE0EC1E48D</string>
	<key>PayloadVersion</key>
	<integer>1</integer>
</dict>
</plist>
```
