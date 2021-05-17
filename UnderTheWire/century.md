## Century 1

The password for Century2 is the build version of the instance of PowerShell installed on this system.

### Note
– The format is as follows: **.*.*****.**** <br>
– Include all periods <br>
– Be sure to look for build version and NOT PowerShell version <br>

### Resolution

To check the powershell version we can use the command $PSVersionTable, which is a read-only hash table that returns information about the Powershell version.

![image](https://user-images.githubusercontent.com/25660910/118482263-64966300-b70c-11eb-91d0-9229af05883e.png)


## Century 2

The password for Century3 is the name of the built-in cmdlet that performs the wget like function within PowerShell PLUS the name of the file on the desktop.

### Note
– If the name of the cmdlet is “get-web” and the file on the desktop is named “1234”, the password would be “get-web1234”. <br>
– The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

Answer: The command we are looking for is... Invoke-WebRequest!


## Century 3

The password for Century4 is the number of files on the desktop.

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118484058-b4762980-b70e-11eb-9664-51de48ab7ca3.png)

To see the number of files that exists in a certain folder we use the command Get-ChildItem -File. This will only show us a list of files so we can add the command Measure-Object

## Century 4

The password for Century5 is the name of the file within a directory on the desktop that has spaces in its name.

### Note
– The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

Here we only have to move to the specified directory

![image](https://user-images.githubusercontent.com/25660910/118484887-a5dc4200-b70f-11eb-9e59-fa37126130b0.png)


## Century 5

The password for Century6 is the short name of the domain in which this system resides in PLUS the name of the file on the desktop.

### Note
– If the short name of the domain is “blob” and the file on the desktop is named “1234”, the password would be “blob1234”.
– The password will be lowercase no matter how it appears on the screen.


