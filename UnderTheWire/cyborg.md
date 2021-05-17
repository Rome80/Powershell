
## Cyborg 0

Credentials - ```Cyborg1:Cyborg1```

## Cyborg 1

The password for cyborg2 is the state that the user Chris Rogers is from as stated within Active Directory. <br>

### Note

- The password will be lowercase no matter how it appears on the screen. <br>
-  “State” refers to the location within the country and NOT the “state” of the account (enabled/ disabled). <br>

### Resolution

The command **Get-ADUser** is used to retrieve the existing users, but we just want the user Chris Rogers, so we added the instruction **-Filter** to the command in order to show only the supposed user. <br>

![image](https://user-images.githubusercontent.com/25660910/118517350-08910600-b72f-11eb-82fa-26577c2beb90.png)

Password - ```kansas```

## Cyborg 2

The password for cyborg3 is the host A record IP address for CYBORG718W100N PLUS the name of the file on the desktop.

### Note
- If the IP is “10.10.1.5” and the file on the desktop is called “_address”, then the password is “10.10.1.5_address”. <br>
- The password will be lowercase no matter how it appears on the screen.

### Resolution

In the image below is the file name.

![image](https://user-images.githubusercontent.com/25660910/118517809-73dad800-b72f-11eb-9a53-2f2eef342903.png)

This was a little tricky, so we had to check the hints given, but it weren't that helpful. So let´s go to google! <br>

So we found out the command **Get-DnsServerResourceRecord**



