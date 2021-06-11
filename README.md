# InfoPuller
CLI application that can extract the details for given website or local machine. It also has basic persistence that might used in malware or threat. It's a personal study project. 🙂

<h2><u>Features overview</u> :</h2>

The <u><i>visible</i></u> key features :
- Extract all of the available IPv4 and IPv6 addresses for given website.
- Fetch response <a href="https://developers.google.com/search/docs/advanced/robots/intro">robots.txt</a> for given website, then save and/or show.
- Extract local machine's available IPv4 and IPv6 addresses.
- Extract <a href="https://en.wikipedia.org/wiki/MAC_address">Media Access Control (MAC)</a> details for local machine, either in <i>basic</i> or in <i>detailed</i> form.

Interesting <u><i>invisible</i></u> key features :
- The app copies itself to other place and becomes hidden.
- Makes changes in Windows registry to autostart things after every system startup.

<h2><u><a href="https://docs.microsoft.com/en-us/windows/win32/api/">Win32</a> API headers</u> :</h2>

<ol>
    <li>
        <a href="https://en.wikipedia.org/wiki/Windows.h">Windows.h</a> - A Windows-specific header file for the C and C++ programming languages which contains declarations for all of the functions in the Windows API.
    </li>
    <li>
        <a href="https://en.wikipedia.org/wiki/C_file_input/output">stdio.h</a> - Provides many standard library functions for input and output.
    </li>
    <li>
        <a href="https://en.wikipedia.org/wiki/C_standard_library">stdlib.h</a> - Provides macros, type definitions and functions for tasks such as string handling, mathematical computations, input/output processing, memory management, and several other operating system services.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/fileapi/">fileapi.h</a> - Used for Data Access and Storage.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/winsock2/">WinSock2.h</a> - Provides useful functions for network programming such as sockets, IP addresses and so on. It is used by <a href="https://docs.microsoft.com/en-us/windows/win32/api/_qos/">Quality of Service (QOS)</a>.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/wininet/">WinInet.h</a> - To handle files over FTP/HTTP URL.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2tcpip/">WS2tcpip.h</a> - WinSock2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/iphlpapi/">iphlpapi.h</a> - Provides functions to get <a href=https://en.wikipedia.org/wiki/MAC_address">MAC address</a> details.
    </li>
</ol>

<h2><u>Features in detail</u> :</h2>

  <h3><b>1. Set website domain :</b></h3>
  <ul> 
    <li>
        On launch, the app opens the console window and makes it maximized having some fancy text representing the name of application, and few numbered menu options to choose from : <BR />
        <p align="center"><img src="AppScreens/Main_app.png" /></p>
    </li>
    <li>
        To get information about website, first set the domain using option '<b>1</b>' (the domain should be in form of <i><a href="http://www.example.com/">www.example.com</a></i> or <i><a href="http://www.example.com/">example.com</a></i>) : <BR />
        <p align="center"><img src="AppScreens/Main_app.png" /></p>
    </li>
    <li>
        Now the website domain is all set; then the other related menu options also get reflected : <BR />
        <p align="center"><img src="AppScreens/Main_app.png" /></p>
        Setting the website domain is essential to get results otherwise one can not use menu options related to website domains : <BR />
        <p align="center"><img src="AppScreens/Main_app.png" /></p>
    </li>
  </ul>

  <h3><b>2. Extract IP details :</b></h3>
  <ul>
    <li>
        If the website domain set properly, program will list of all available IPv4 and IPv6 addresses and if any of IPv4 or IPv6 is not available, then useful message with related error code is returned : <BR />
        <p align="center"><img src="AppScreens/Main_app.png" /></p>
    </li>
  </ul>

  