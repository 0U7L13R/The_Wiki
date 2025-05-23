Use: Java-based framework for web app pen testing

# Modules
Proxy: Enables interception/modification of requests/responses while interacting with web apps
Repeater: For capturing/modifying/resending the same request multiple times. Useful when crafting payloads trhough trial and error or testing endpoints for vulnerabilities
Intruder: Spraying endpoints with requests, commonly used for fuzz/brute force endpoints
Decoder: Can decode captured info or encode payloads before sending to the target
Comparer: Compares two pieces of data at either word or byte level
Sequencer: Used when assessing randomness of tokens - session cookie values or othe randomly generated data. If the algorithm used for generating these values lacks secure randomness, it can expose avenues for  attacks


# Dashboard
Tasks: The Tasks menu allows you to define background tasks that Burp Suite will perform while you use the application. In Burp Suite Community, the default “Live Passive Crawl” task, which automatically logs the pages visited, is sufficient for our purposes in this module. Burp Suite Professional offers additional features like on-demand scans.
Event log: The Event log provides information about the actions performed by Burp Suite, such as starting the proxy, as well as details about connections made through Burp.
Issue Activity: This section is specific to Burp Suite Professional. It displays the vulnerabilities identified by the automated scanner, ranked by severity and filterable based on the certainty of the vulnerability.
Advisory: The Advisory section provides more detailed information about the identified vulnerabilities, including references and suggested remediations. This information can be exported into a report. In Burp Suite Community, this section may not show any vulnerabilities.


| Shortcuts | tab|
|-----------|----|
| Ctrl + Shift + D | Dashboard |
| Ctrl + Shift + T | Target tab |
| Ctrl + Shift + P | Proxy tab |
| Ctrl + Shift + I | Intruder tab |
| Ctrl + Shift + R | Repeater tab |

