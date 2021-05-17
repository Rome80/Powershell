## Century 1

The password for Century2 is the build version of the instance of PowerShell installed on this system.

### Note
- The format is as follows: **.*.*****.**** <br>
- Include all periods <br>
- Be sure to look for build version and NOT PowerShell version <br>

### Resolution

To check the powershell version we can use the command $PSVersionTable, which is a read-only hash table that returns information about the Powershell version. <br>

![image](https://user-images.githubusercontent.com/25660910/118482263-64966300-b70c-11eb-91d0-9229af05883e.png)

Password - ```5.1.14393.3866``` <br>

## Century 2

The password for Century3 is the name of the built-in cmdlet that performs the wget like function within PowerShell PLUS the name of the file on the desktop. <br>

### Note
- If the name of the cmdlet is “get-web” and the file on the desktop is named “1234”, the password would be “get-web1234”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

Answer: The command we are looking for is... ```Invoke-WebRequest``` <br>


## Century 3

The password for Century4 is the number of files on the desktop. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118484058-b4762980-b70e-11eb-9664-51de48ab7ca3.png)

To see the number of files that exists in a certain folder we use the command Get-ChildItem -File. This will only show us a list of files so we can add the command Measure-Object <br>

Password - ```123``` <br>
 
## Century 4

The password for Century5 is the name of the file within a directory on the desktop that has spaces in its name. <br>

### Note
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

Here we only have to move to the specified directory <br>

![image](https://user-images.githubusercontent.com/25660910/118484887-a5dc4200-b70f-11eb-9e59-fa37126130b0.png)

Password - ```61580``` <br>

## Century 5

The password for Century6 is the short name of the domain in which this system resides in PLUS the name of the file on the desktop. <br>

### Note
- If the short name of the domain is “blob” and the file on the desktop is named “1234”, the password would be “blob1234”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

First, let's start with the easy part! Let's see the name of the file located in the Desktop directory. <br>

![image](https://user-images.githubusercontent.com/25660910/118491093-8bf22d80-b716-11eb-8923-c7dc6aa05845.png)

After the file's name has been found (3347), we have to find a way to find out the domain name. With the cmdlet Get-WmiObect, we can obtain some information related to the system. For example, we can retrieve information about local processes. <br>

![image](https://user-images.githubusercontent.com/25660910/118492692-2c951d00-b718-11eb-9ce1-835c17d3301c.png)

Password - ```underthewire3347``` <br>

## Century 6

The password for Century7 is the number of folders on the desktop. <br>

### Resolution

As seen before withe the command Get-ChildItem we can get a list of files or folders, depending on the instruction used. In this case, to retrieve the number of folders, we use the instruction -Directory. <br>

![image](https://user-images.githubusercontent.com/25660910/118494770-68c97d00-b71a-11eb-9cb4-9ed63330075a.png)

Password - ```197``` <br>

## Century 7

The password for Century8 is in a readme file somewhere within the contacts, desktop, documents, downloads, favorites, music, or videos folder in the user’s profile. <br>

### Note

- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

To find this file, we used some additional instructions to the Get-ChildItem command: <br>
- Recurse: to search sub-directories <br>
- Error Action SIlentlyContinue: to not display the error <br>

![image](https://user-images.githubusercontent.com/25660910/118496784-5b14f700-b71c-11eb-9ea1-754eb8ca0655.png)

And inside the file we have: <br>

![image](https://user-images.githubusercontent.com/25660910/118499382-c8c22280-b71e-11eb-83e7-b8964a8990fc.png)

Password - ```7points``` <br>


## Century 8

The password for Century9 is the number of unique entries within the file on the desktop. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118500477-b85e7780-b71f-11eb-9679-1a8dfed7ed4b.png)

The command Get-Content will display to us the content of a certain file. We had to add the instruction sort in order to use the command Get-Unique, which allow us to see only the unique entries. Finally to count those unique entries we had the command Measure-Object. <br>

Password - ```696``` <br>

## Century 9

The password for Century10 is the 161st word within the file on the desktop. <br>

### Note

- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

First let's check the item in the desktop directory <br>

![image](https://user-images.githubusercontent.com/25660910/118500820-06737b00-b720-11eb-8eb0-3af828004ae1.png)

Then we had to see what was the content of that file <br>

![image](https://user-images.githubusercontent.com/25660910/118501301-78e45b00-b720-11eb-8126-5233f745d337.png)

And finally, in order to simplify the text format, we used the instruction Delimiter to put print a word by line. After that with the instruction "TotalCount 161", we were able to print 161 words in order to achieve the pruposed goal. <br>

![image](https://user-images.githubusercontent.com/25660910/118501810-0162fb80-b721-11eb-8614-0ec27e0ed5b9.png)

Password - ```pierid``` <br>

## Century 10

The password for Century11 is the 10th and 8th word of the Windows Update service description combined PLUS the name of the file on the desktop. <br>

### Note

- The password will be lowercase no matter how it appears on the screen. <br>
- If the 10th and 8th word of the service description is “apple” and “juice” and the name of the file on the desktop is “88”, the password would be “applejuice88”. <br>

### Resolution

The  file located in the desktop directory is: <br>

![image](https://user-images.githubusercontent.com/25660910/118503417-83075900-b722-11eb-98ac-6603509e117d.png)

To get the Windows Update service description, we had to find out what was the name of the service (wuauserv). After that, we use the command Get-WmiObject, where the object selected was the update service. <br>

![image](https://user-images.githubusercontent.com/25660910/118508136-cf549800-b726-11eb-87d5-2e33718fdd87.png)

The 10th word: ```windows``` <br>
The 8th word: ```updates``` <br>
The password: ```windowsupdates110``` <br>

## Century 11

The password for Century12 is the name of the hidden file within the contacts, desktop, documents, downloads, favorites, music, or videos folder in the user’s profile. <br>

### Note
- Exclude “desktop.ini”. <br>
- The password will be lowercase no matter how it appears on the screen. <br>

### Resolution

![image](https://user-images.githubusercontent.com/25660910/118509476-f8295d00-b727-11eb-80b3-72e7a6e99200.png) 

With the specified command we were able to obtain the hidden file (secret_sauce) <br>

![image](https://user-images.githubusercontent.com/25660910/118509547-08413c80-b728-11eb-9ded-6ed1c73070f0.png) <br>

Password - ```secret_sauce``` <br>

## Century 12

The password for Century13 is the description of the computer designated as a Domain Controller within this domain PLUS the name of the file on the desktop. <br>

### Note
- The password will be lowercase no matter how it appears on the screen. <br>
- If the description “today_is” and the file on the desktop is named “_cool”, the password would be “today_is_cool”. <br>

### Resolution

The file within the desktop directory is called '_thing'. <br>

Then we had to get the name of the domain controller, as showned in the image below <br>

![image](https://user-images.githubusercontent.com/25660910/118510827-3bd09680-b729-11eb-9f1b-2235129b002e.png) <br>

And finally, we could obtain through the instruction Properties, the description of the computer <br>

![image](https://user-images.githubusercontent.com/25660910/118510971-5f93dc80-b729-11eb-9a25-c34974538e99.png) <br>

Password - ```i_authenticate_thing``` <br>


## Century 13

The password for Century14 is the number of words within the file on the desktop. <br>

### Resolution

To get the number of words within the file "countmywords" we used again the instruction delimiter to show a word per line and the we count the number of lines that existed in the file. <br>

![image](https://user-images.githubusercontent.com/25660910/118511339-b8fc0b80-b729-11eb-82eb-435266ff1fa3.png)

Password - ```755``` <br>


## Century 14

The password for Century15 is the number of times the word “polo” appears within the file on the desktop. <br>

### Note
- You should count the instances of the whole word only... <br>

### Resolution

With this command, we were able to select the string that match with the word "polo" and then with the command count, it counts the number of ocorrences of the word "polo". <br>

![image](https://user-images.githubusercontent.com/25660910/118511938-46d7f680-b72a-11eb-979e-78d2ad11bd11.png)

Password - ```rowray_timer``` <br>


