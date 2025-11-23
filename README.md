# DNSteal (Python 3 Modernized)

> ⚠️ **Note:** This is an updated fork of the original [m57/dnsteal](https://github.com/m57/dnsteal).
> It has been ported to **Python 3** and patches several bugs found in modern environments.

### Why I made this
I use this tool for a cybersecurity course. The original code was written in Python 2. Since that version is End-of-Life, I ported it to Python 3 to make it easier to use on modern systems.

I used standard migration tools like [2to3](https://docs.python.org/3.12/library/2to3.html) and [autopep8](https://pypi.org/project/autopep8/) as a base. Then, I manually fixed the network logic to handle bytes and strings correctly.

###  Key Changes in this Version:
* **Python 3 Port:** Full migration from Python 2 (syntax, print functions, exception handling).
* **Network Stability:** Fixed critical `TypeError` bugs by strictly handling bytes/strings for socket transmission.
* **Modern `dig` Compatibility:** Added the `+noidnin` flag to generated commands. This fixes the "illegal IDNA2008 name" error on modern Linux distributions when payloads end with a hyphen (`-.`).
* **Bug Fixes:** Fixed MD5 checksum crash by enforcing binary mode (`rb`) for file reading.
* **Cleanup:** Refactored code to comply with PEP8 standards and removed unused imports.

---