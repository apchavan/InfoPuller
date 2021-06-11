# InfoPuller
CLI application that can extract the details for given website or local machine. It also has basic persistence that might used in malware or threat. It's just a personal study project ;-)

The <u><i>visible</i></u> key features :
- Extract all of the available IPv4 and IPv6 addresses for given website (for e.g. 'www.example.com' or 'example.com').
- Fetch response <a href="https://developers.google.com/search/docs/advanced/robots/intro">robots.txt</a> for given website, then save and/or show.
- Extract local machine's available IPv4 and IPv6 addresses (could be combination of local and global IP).
- Extract <a href="https://en.wikipedia.org/wiki/MAC_address">Media Access Control (MAC)</a> details for local machine, either in <i>basic</i> form or in <i>detailed</i> form.

Interesting <u><i>invisible</i></u> key features :
- The app copies itself to other place and becomes hidden.
- Makes changes in Windows registry to autostart things after every system startup.

<h2><u>Development</u> :</h2>
The <i>core</i> Windows libraries used here are:
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
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2tcpip/">WS2tcpip.h</a> - WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.
    </li>
    <li>
        <a href="https://docs.microsoft.com/en-us/windows/win32/api/iphlpapi/">iphlpapi.h</a> - Provides functions to get <a href=https://en.wikipedia.org/wiki/MAC_address">MAC address</a> details.
    </li>
</ol>

<BR />

