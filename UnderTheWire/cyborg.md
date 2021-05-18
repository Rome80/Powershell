
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

So we found out the command **Get-DnsServerResourceRecord** and we added the instruction **-RRType A**, that returns all the A records from a specified zone. <br>

![image](https://user-images.githubusercontent.com/25660910/118615918-2145fe00-b7b9-11eb-8357-9a2d9d1cd82a.png)

Password - ```172.31.45.167_ipv4```


## Cyborg 3

The password for cyborg4 is the number of users in the Cyborg group within Active Directory PLUS the name of the file on the desktop. <br>

### Note

- If the number of users is “20” and the file on the desktop is called “_users”, then the password is “20_users”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118618718-cfeb3e00-b7bb-11eb-9657-a8eb1c595975.png)

To retrieve the full list of users that belong to the group Cyborg from the domain, we can use the command **Get-AGroupMember -Identity 'cyborg'**. But that only display all the existing users, so we added the instruction **count** <br>

![image](https://user-images.githubusercontent.com/25660910/118617490-98c85d00-b7ba-11eb-9503-5ebb27a6529f.png)

Password - ```88_objects```


## Cyborg 4

The password for cyborg5 is the PowerShell module name with a version number of 8.9.8.9 PLUS the name of the file on the desktop.

### Note

- If the module name is “bob” and the file on the desktop is called “_settings”, then the password is “bob_settings”.
- The password will be lowercase no matter how it appears on the screen.

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118618809-e5f8fe80-b7bb-11eb-9538-3fb9a1f6e875.png)

I got a little stuck in here, so first things first, let's follow the hints.

![image](https://user-images.githubusercontent.com/25660910/118618944-0aed7180-b7bc-11eb-8322-b3fbece093ab.png)

With this command, we could see the versions of the different modules

![image](https://user-images.githubusercontent.com/25660910/118619147-396b4c80-b7bc-11eb-9738-6a2074150fb2.png)

Password - ```bacon_eggs```

## Cyborg 5

The password for cyborg6 is the last name of the user who has logon hours set on their account PLUS the name of the file on the desktop.

### Note
-  If the last name is “fields” and the file on the desktop is called “_address”, then the password is “fields_address”. <br>
-  The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118622405-332a9f80-b7bf-11eb-89af-763239416a49.png)

Once again, we used the command **Get-ADUser**, but with some additional instructions... The instruction **Properties** to display the logonhours and then with the command **where-object** we selected the logonhours that were defined or greater than 0.

![image](https://user-images.githubusercontent.com/25660910/118627439-a0403400-b7c3-11eb-9feb-35a5d0c2ff26.png)

Password - ```rowray_timer```


## Cyborg 6

The password for cyborg7 is the decoded text of the string within the file on the desktop. <br>

### Note
- The password is the last word of the string. For example, if it is “I like PowerShell”, the password would be “powershell”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>
- There are no spaces in the answer. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118629128-33c63480-b7c5-11eb-8795-659dbd96bb86.png)

Well... No cmdlet available, so we had to talk with google. The command is presented below <br>

![image](https://user-images.githubusercontent.com/25660910/118629318-62dca600-b7c5-11eb-9ca3-2fc171641fa2.png)

Password - ```cybergeddon```

## Cyborg 7

The password for cyborg8 is the executable name of a program that will start automatically when cyborg7 logs in. <br>

### Note
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

To achieve this solution, once again we had to google it. We found the command **Get-CimInstance Win32_StartupCommand**. This command is used to get the CIM (Common Information Model) instances of a class from a CIM Server. It can be added some instructions to this command like the **Win32_StartupCommand** that it's used to find the startup applications.

![image](https://user-images.githubusercontent.com/25660910/118633912-e39da100-b7c9-11eb-9de2-eba8d1467966.png)

Password - ```skynet```

## Cyborg 8

The password for cyborg9 is the Internet zone that the picture on the desktop was downloaded from.

### Note
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

We needed to access to the image's metadata. After some research, we found the command **Get-Item -Stream**. The instruction -stream allows us to get specified alternate NTFS file streams from the file, such as the zone identifier! <br>

![image](https://user-images.githubusercontent.com/25660910/118643466-7fcca580-b7d4-11eb-9a5b-c6ff3050757c.png)


Password - ```4```

## Cyborg 9

The password for cyborg10 is the first name of the user with the phone number of 876-5309 listed in Active Directory PLUS the name of the file on the desktop. <br>

### Note
- If the first name “chris” and the file on the desktop is called “23”, then the password is “chris23”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118667854-41db7b80-b7ec-11eb-8ba0-32fbe8967d75.png)

Then, we had to filter the properties through the phone number. After some research, we were able to filter through the field **telephonenumber** <br>

![image](https://user-images.githubusercontent.com/25660910/118667230-bb269e80-b7eb-11eb-8c50-6d9109b9f219.png)

Password - ```onita99```


## Cyborg 10

The password for cyborg11 is the description of the Applocker Executable deny policy for ill_be_back.exe PLUS the name of the file on the desktop. <br>

### Note
- If the description is “green$” and the file on the desktop is called “28”, then the password is “green$28”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>


### Resolution







