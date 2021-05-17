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
– The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

First, let's start with the easy part! Let's see the name of the file located in the Desktop directory

![image](https://user-images.githubusercontent.com/25660910/118491093-8bf22d80-b716-11eb-8923-c7dc6aa05845.png)

After the file's name has been found (3347), we have to find a way to find out the domain name. With the cmdlet Get-WmiObect, we can obtain some information related to the system. For example, we can retrieve information about local processes

![image](https://user-images.githubusercontent.com/25660910/118492692-2c951d00-b718-11eb-9ce1-835c17d3301c.png)

Password - underthewire3347

## Century 6

The password for Century7 is the number of folders on the desktop.	

### Resolution

As seen before withe the command Get-ChildItem we can get a list of files or folders, depending on the instruction used. In this case, to retrieve the number of folders, we use the instruction -Directory

![image](https://user-images.githubusercontent.com/25660910/118494770-68c97d00-b71a-11eb-9cb4-9ed63330075a.png)

Password - 197

## Century 7

The password for Century8 is in a readme file somewhere within the contacts, desktop, documents, downloads, favorites, music, or videos folder in the user’s profile.

### Note

The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

To find this file, we used some additional instructions to the Get-ChildItem command:
- Recurse: to search sub-directories
- Error Action SIlentlyContinue: to not display the error

![image](https://user-images.githubusercontent.com/25660910/118496784-5b14f700-b71c-11eb-9ea1-754eb8ca0655.png)

And inside the file we have:

![image](https://user-images.githubusercontent.com/25660910/118499382-c8c22280-b71e-11eb-83e7-b8964a8990fc.png)


## Century 8

The password for Century9 is the number of unique entries within the file on the desktop.

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118500477-b85e7780-b71f-11eb-9679-1a8dfed7ed4b.png)

The command Get-Content will display to us the content of a certain file. We had to add the instruction sort in order to use the command Get-Unique, which allow us to see only the unique entries. Finally to count those unique entries we had the command Measure-Object.


## Century 9

The password for Century10 is the 161st word within the file on the desktop.

### Note

– The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

First let's check the item in the desktop directory

![image](https://user-images.githubusercontent.com/25660910/118500820-06737b00-b720-11eb-8eb0-3af828004ae1.png)

Then we had to see whtat was the content of that file

![image](https://user-images.githubusercontent.com/25660910/118501301-78e45b00-b720-11eb-8126-5233f745d337.png)

And finally, in order to simplify the text format, we used the instruction Delimiter to put print a word by line. After that with the instruction "TotalCount 161", we were able to print 161 words in order to achieve the pruposed goal.

![image](https://user-images.githubusercontent.com/25660910/118501810-0162fb80-b721-11eb-8614-0ec27e0ed5b9.png)

The password is: pierid

## Century 10

The password for Century11 is the 10th and 8th word of the Windows Update service description combined PLUS the name of the file on the desktop.

### Note

– The password will be lowercase no matter how it appears on the screen.
– If the 10th and 8th word of the service description is “apple” and “juice” and the name of the file on the desktop is “88”, the password would be “applejuice88”. <br>

### Resolution
