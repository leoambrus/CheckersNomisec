# CheckersNomisec
In all the NomiSec repository there are some checkers that aren't PoC and here they are described as what they are. Checkers.
-----------------------------------------------------------------------------------------------------------------------------------------
1- CVE-2023-36884 Checker
(https://github.com/tarraschk/CVE-2023-36884-Checker)   

The code is just a PowerShell script that checks whether a system is vulnerable to CVE-2023-36884.
The code works by checking whether the system is running Microsoft-provided mitigations for this vulnerability. If the system is not performing the mitigations, the PoC will display a warning. It is used to help users identify whether their systems are vulnerable to a particular vulnerability.
If the system is not performing the mitigations, the code will display a warning.

-----------------------------------------------------------------------------------------------------------------------------------------
2- 2022/CVE-2022-20866.json  Checker
(https://github.com//CiscoPSIRT//CVE-2022-20866) 

The code checks whether an RSA private key contained in a PKCS12 file is vulnerable to a specific flaw. The flaw in question is referenced in the code as "Cisco RSA Private Key Leak Vulnerability (CVE-2022-20866)".
Verification is done based on two characteristics of the private key:

Private key validity: The code checks whether the private key is valid or not. If the key is invalid, it prints a corresponding message.

Insufficient size of key components: It also checks whether the key components (such as prime numbers, exponents, and others) have sizes that can be considered insufficient in relation to the size of the key modulus. This can make the key vulnerable to attack.

If the private key is found to be invalid or has short components, the code issues a warning about the vulnerability but does not perform any attacks or exploits. Instead, it provides information about the key that can be used to make decisions about replacing the key or implementing additional security measures.

the code does not exploit the flaw, but only verifies the validity of the private key and its compliance with security standards.


-----------------------------------------------------------------------------------------------------------------------------------------
3- 2015/CVE-2015-0204.json  Checker
(https://github.com//felmoltor//FreakVulnChecker) 

This is a Bash script that checks whether a server is accepting EXPORT cipher suites that may be vulnerable to the FREAK attack (CVE-2015-0204). 
The script checks whether the server supports EXPORT cipher suites and records the results in a CSV file with the name in the format `YYYYMMDD_HHMMSS_freak.check.output.csv`.
The purpose of this script is to help identify servers that are vulnerable to the FREAK attack, allowing administrators to take steps to reconfigure their servers and disable acceptance of EXPORT cipher suites.


-----------------------------------------------------------------------------------------------------------------------------------------
4- 2015/CVE-2015-3825.json Checker? Deprecated? Broken link?
(https://github.com//roeeh//conscryptchecker) 

Supposedly
 
This app verifies if your device is still vulnerable to CVE-2015-3825 / CVE-2015-3837, aka "One Class to Rule Them All", by checking if it contains the vulnerable conscrypt's OpenSSLX509Certificate class. A patch was released in August 2015 by Google.

There are four codes here, they are scripts used in the Android development environment with the Gradle tool. I will explain each of them briefly:

1- build.gradle (top-level build file):

This file is used to configure options common to all subprojects or modules in an Android project. Here are some of the actions performed on this file:

Defines the Maven repositories to be used, mainly jcenter() which is a central repository for Java libraries.
Defines Gradle dependencies, including the Gradle plugin version (com.android.tools.build:gradle) and the google-services version.
Instructs that application-specific dependencies must be included in individual module build files.

2-gradlew (Linux/Mac):

This is a Gradle startup script for Unix-based operating systems. It is used to initiate Gradle tasks such as compiling, running tests, and building packages. This script checks the Java and Gradle installation, sets environment variables, and starts Gradle with the specified options.

3-gradlew.bat (Windows):

This is the equivalent of the gradlew script for Windows systems. It does the same actions as the gradlew script, but in the Windows environment.

4-settings.gradle:

The settings.gradle file is used to define the global configuration of the Gradle project, including the modules or subprojects that are part of the project. The example provided (include ':app') indicates that the project includes a single module called "app".

These scripts are an integral part of a typical Android project built with Gradle. They allow you to configure dependencies, build tasks, and other project settings in a structured and automated way. Gradle is a widely used tool in Android development to manage project build and dependencies.

The link for the app on playstore is broken. I find this one.
https://apkcombo.com/conscryptchecker/roeeh.conscryptchecker/

VIDEO NOT AVAIABLE
LINK FOR THE GOOGLEPLAY  USER NOT AVAIABLE




-----------------------------------------------------------------------------------------------------------------------------------------
5- 2017/CVE-2017-6558.json Checker
(https://github.com//GemGeorge//iBall-UTStar-CVEChecker) 

This code does not exploit the vulnerability,it is a "checker" or vulnerability scanner. It checks whether a network device is vulnerable to three specific vulnerabilities: CVE-2017-6558, CVE-2017-14243, and CVE-2017-14244. The code does not perform any active exploitation or exploitation of these vulnerabilities; instead, it checks whether certain conditions and indicators of these vulnerabilities are present on a target device.

What the code does is the following:

1. Makes an HTTP request to the device URL provided as an argument.
2. Analyzes the response to determine the device type and its firmware version.
3. Based on the device identification and firmware version, it determines whether the device is vulnerable to one of the three listed vulnerabilities.
4. If the device is vulnerable, it displays information about the device, including the default login credentials, if applicable.
5. If the device is not vulnerable to any of the vulnerabilities, it reports that the device is not vulnerable.

In short, the code is used to check whether a device is vulnerable to specific vulnerabilities and display information about the device, but it does not perform any exploits or attacks against the device. It is a tool for security checking purposes.

-----------------------------------------------------------------------------------------------------------------------------------------
6- 2015/CVE-2015-0235.json  Checker
(https://github.com//fser//ghost-checker) 

This code is primarily a checker rather than an exploit. Its purpose is to identify whether the system's `gethostbyname_r` function is vulnerable to a specific type of vulnerability related to buffer overflow.

The code does the following:

1. Calls the `gethostbyname_r` function with certain inputs.
2. Checks the return value `retval` to see if it equals `ERANGE`, which would indicate that the buffer provided to the function was too small.
3. Verifies whether the `temp.canary` value has been modified. If it has been modified, it assumes that the vulnerability exists.

If the `CANARY` value is modified, it suggests a potential vulnerability. If `retval` is `ERANGE`, it implies that the system is not vulnerable. However, this code does not actively exploit any vulnerability or perform any malicious actions. It is a diagnostic tool used to determine the presence of a specific type of vulnerability.

-----------------------------------------------------------------------------------------------------------------------------------------
7- 2022/CVE-2022-22965.json Checker
(https://github.com//alt3kx//CVE-2022-22965) 

This script is primarily a checker for the CVE-2022-22965 vulnerability in Spring Framework versions 5.2.x and 5.3.x. It checks whether a given target is vulnerable to this specific vulnerability by sending a specific payload and analyzing the response. It doesn't actively exploit the vulnerability but rather assesses whether the vulnerability is present based on the target's response.

In summary, it's a checker, not a vulnerability explorer or exploiter.

-----------------------------------------------------------------------------------------------------------------------------------------
8- 2020/CVE-2020-3452.json Checker
(https://github.com//faisalfs10x//Cisco-CVE-2020-3452-shodan-scanner) 

This script is a checker, not an exploit. It's designed to check for the presence of the Cisco ASA CVE-2020-3452 vulnerability in Cisco ASA devices. The script uses Shodan to identify Cisco ASA devices based on their ASN (Autonomous System Number) and then attempts to verify if they are vulnerable by making a specific HTTP request and checking the response. If the response indicates the presence of the vulnerability, it reports the target as vulnerable; otherwise, it reports the target as not vulnerable.

-----------------------------------------------------------------------------------------------------------------------------------------
9- 2022/CVE-2022-0847.json Checker
(https://github.com//basharkey//CVE-2022-0847-dirty-pipe-checker) 

The Bash scripts are checkers. They are used to check whether a Linux kernel version is vulnerable based on certain version criteria. These scripts do not perform any exploitation or attack; instead, they help determine the vulnerability status of a given kernel version.

-----------------------------------------------------------------------------------------------------------------------------------------
10- 2021/CVE-2021-41773.json Checker
(https://github.com//jheeree//Simple-CVE-2021-41773-checker)

This Bash script is a checker for the CVE-2021-41773 vulnerability in Apache HTTP Server. This vulnerability allows an attacker to access sensitive files on the server due to a misconfiguration in the server's mod_proxy module.
Here's what the script does:

1. It takes an input file (hosts.txt) containing a list of IP addresses or hostnames to check for vulnerability.

2. It sends HTTP GET requests to the specified hosts with a specially crafted request path to check if they are vulnerable to the CVE-2021-41773 exploit.

3. For each host, it checks if the response contains the content of the "/etc/passwd" file, which would indicate a vulnerable host.

4. It creates a report.txt file in a directory named with the current date and time to record the results.

5. It prints a summary of the total number of hosts found to be vulnerable and not vulnerable.

In summary, this script is designed to quickly identify whether a list of hosts is vulnerable to the CVE-2021-41773 vulnerability in the Apache HTTP Server. If the script finds that a host is vulnerable, it marks it as such in the report file.

-----------------------------------------------------------------------------------------------------------------------------------------
11- 2015/CVE-2015-1635.json Checker
(https://github.com//xPaw//HTTPsys) 

This PHP script is just a vulnerability checker. It does not exploit any vulnerabilities or perform any malicious actions. Its primary purpose is to determine whether a server is vulnerable to the CVE-2015-1635 (MS15-034) vulnerability, which is a security flaw in the HTTP.sys component of Windows. It sends a specially crafted HTTP request to the server to check if it responds in a way that indicates the presence of the vulnerability. Depending on the response, it classifies the server as vulnerable, not vulnerable, or patched.
1-It defines a PHP class called VulnStatus with constants representing different vulnerability statuses. These statuses include vulnerable, not vulnerable, patched, and more.


2-The script receives a URL or hostname as a query parameter (host) via a GET request.


3-It parses the URL and checks if it includes a port number. If not, it assumes port 80.


4-It creates a cache key based on the URL and port to store the vulnerability status.


5-It uses the Memcached library to check if the vulnerability status for the given URL and port is cached. If not, it proceeds to test the vulnerability.


6-It attempts to open a socket connection to the specified host and port.


7-If the connection succeeds, it sends an HTTP GET request with a specially crafted header to test for the presence of the CVE-2015-1635 vulnerability.


8-Depending on the response received, it determines the vulnerability status and caches it for future use.


9-It generates an HTML page with a form where users can input a URL or hostname to check for the vulnerability.


10-After checking, it displays the result as an alert message indicating the vulnerability status. The result is also cached for five minutes.

In summary, it helps users assess the security of a server by checking for a known vulnerability, but it does not take advantage of or exploit the vulnerability in any way.

-----------------------------------------------------------------------------------------------------------------------------------------
12- 2020/CVE-2020-6287.json Checker
(https://github.com//qmakake//SAP_CVE-2020-6287_find_mandate) 

This Bash code is a tool that checks if an account is valid in an SAP WebGUI system. It does this by trying to log into a series of accounts and checking HTTP responses. It is not a “Proof of Concept” (PoC) because it does not demonstrate a vulnerability or exploit a security flaw; rather, it is an account verification tool that tests whether the login credentials provided are valid in the SAP WebGUI system.

-----------------------------------------------------------------------------------------------------------------------------------------
13-2022/CVE-2022-1386.json Checker
(https://github.com//im-hanzou//fubucker) 

The two Bash scripts are tools for checking the CVE-2022-1386 vulnerability in the Fusion Builder plugin on WordPress sites.

The first script, “Single Target Exploiter”, scans a single target for vulnerability. It prompts the user to provide a destination URL and payload URL. The script checks whether the site is vulnerable by sending an HTTP POST request to "admin-ajax.php" with a malicious payload. If the site is vulnerable, it will show the result of the exploit.

The second script, “CVE-2022-1386 Mass Vulnerability Checker”, is used to check a list of URLs for vulnerability. It reads the URLs from a list file and runs checks in parallel to speed up the process. Vulnerable URLs are recorded in a file called "vuln.txt", and non-vulnerable URLs are recorded in "notvuln.txt".

Both scripts are used to check for the presence of the CVE-2022-1386 vulnerability on WordPress sites using the Fusion Builder plugin. They are not exploits; instead, they check the vulnerability and record the results.

-----------------------------------------------------------------------------------------------------------------------------------------
14- 2016/CVE-2016-8467.json   Checker? Deprecated? Broken link?
(https://github.com//roeeh//bootmodechecker)  

It seems like an app developed in Java that checks if your Nexus 6/6P is still vulnerable to CVE-2016-8467 and/or if your bootmode property has been tampered with.
At this repository there are some gradlew files that describe the app and that’s all.
I can’t say if it is a checker or not because i don’t have a working app to use and tell.

The link for playstore is broken:
https://play.google.com/store/apps/details?id=roeeh.bootmodechecker

-----------------------------------------------------------------------------------------------------------------------------------------
15- 2015/CVE-2015-6835.json Checker and PoC
(https://github.com//ockeghem//CVE-2015-6835-checker) 

This PHP code is an example of exploitation of a known vulnerability called CVE-2015-6835. To understand what the code does, let's break it down into parts:

1- Class1 Class Definition:
A class called Class1 is defined.
Inside the class, there is a __destruct() method which is a magic method in PHP. This method is automatically called when an object of the class is destroyed. However, in this case, the method was defined to print the message "CVE-2015-6835 vulnerable" when the object is destroyed.

2- Creating Manipulated Session Data:
The $sessdata variable contains manipulated session data in string format. This session data is crafted to exploit the CVE-2015-6835 vulnerability. They include an entry that appears to be a serialization of an object of class Class1.

3- Session Start:
session_start() is called to start a PHP session.

4- Session Decoding:
session_decode($sessdata) is used to decode the session data provided in the $sessdata variable. Manipulation of session data, especially the inclusion of serialization of an object of class Class1, is designed to trigger the vulnerability.

5- Session Data Printing:
var_dump($_SESSION) is used to display the decoded session data on the screen.

6- Session Destruction:
session_destroy() is called to destroy a PHP session.

The main purpose of this code is to demonstrate the vulnerability CVE-2015-6835, which is related to the manipulation of serialized data in PHP sessions. The code exploits this vulnerability by including the serialization of a Class1 class object in the session data and then printing the session state. The result of the execution will be the printout of the message "CVE-2015-6835 vulnerable", implying that the vulnerability was successfully exploited.

-----------------------------------------------------------------------------------------------------------------------------------------
16- 2021/CVE-2021-36934.json Checker
(https://github.com//irissentinel//CVE-2021-36934) 

This PowerShell code appears to be a "Checker". It is not malicious code, but rather a tool that scans and, if necessary, patches systems for the known vulnerability CVE-2021-36934, also known as HiveNightmare. I will explain why he is classified as a "Checker":

1- Description and Documentation: Code starts with a clear description of what it does and what its purpose is. He also credits the authors with the inspirations for the verification methodology.

2- Vulnerability Check: The code checks the operating system version to determine whether it may be affected by the CVE-2021-36934 vulnerability.

3- File Access Check: The code checks access rights to system files, especially system registry (hive) configuration files such as SAM, SYSTEM and SECURITY. It checks whether the access rights contain a dangerous ACL (Access Control List) that could be exploited.

4- Permissions Patch: If dangerous access rights are found, the code applies Microsoft-recommended permissions patches to mitigate the vulnerability.

5- Shadow Copy Checking and Removal: The code also checks the system for shadow copies, and if shadow copies with dangerous file references are found, the code deletes them to prevent exploitation of the vulnerability.

6- Restore Point Creation: After corrections, the code creates a new restore point, which is a security best practice to facilitate system recovery after changes.

In short, this PowerShell code is a scan and fix tool that aims to protect systems against the CVE-2021-36934 (HiveNightmare) vulnerability. It is not malicious code, but rather a security tool that helps mitigate a known threat. Therefore, it is classified as a "Checker" due to its security checking and patching nature.

-----------------------------------------------------------------------------------------------------------------------------------------
17- 2021/CVE-2021-26084.json Checker
(https://github.com//1ZRR4H//CVE-2021-26084)   

This is a single-line command that checks for the presence of a known vulnerability, CVE-2021-26084, in Atlassian Confluence across multiple servers in bulk. I will explain the command in detail:

1- ‘cat confluence_servers.txt’: This reads the contents of the file called "confluence_servers.txt". Presumably this file contains a list of target servers that you want to scan in bulk.

2- ‘| while read host do; do’: This part of the command reads each line from the "confluence_servers.txt" file and assigns the value of each line to the host variable. The do keyword indicates the start of a loop.

3- ‘curl --connect-timeout 10 --max-time 60 --path-as-is --silent --insecure --user-agent "Mozilla/5.1 (Windows NT 6.1; Win64; x64; rv:59.0) Gecko/ 20100101 Firefox/59.0"’: This is a curl command that makes an HTTP request to each server in the list. Here are the options used:

--connect-timeout 10: Sets a connection timeout of 10 seconds.
--max-time 60: Sets a total time limit of 60 seconds for the operation.
--path-as-is: Allows the path in the URL to be used as is, without encoding.
--silent: Makes curl silent and not display additional information.
--insecure: Ignores SSL certificate errors, making the connection insecure.
--user-agent "Mozilla/5.1 (Windows NT 6.1; Win64; x64; rv:59.0) Gecko/20100101 Firefox/59.0": Sets a "User-Agent" header that mimics a Firefox browser on a Windows system.
4- ‘"https://$host/pages/createpage-entervariables.action?SpaceKey=x"’: This is the URL that curl will access on each server. $host is replaced with the current value of the host variable in the loop. It accesses a specific page in Confluence that is associated with the CVE-2021-26084 vulnerability.

5- ‘| grep -q 'action="doenterpagevariables.action"'’: The result of the HTTP request is passed to grep, which searches for the string 'action="doenterpagevariables.action"'. The -q causes grep not to print the result on the screen, it just checks for the presence of the string.
6- ‘&& printf "$host \033[1;35m Vulnerable\e[0m\n"’: If the string 'action="doenterpagevariables.action"' is found, this indicates that the server is vulnerable. In this case, the "Vulnerable" message is printed in red (\033[1;35m) along with the hostname. Otherwise || printf "$host \033[1;32mOK\e[0m\n" is executed, indicating that the server is not vulnerable. "OK" is printed in green (\033[1;32m).

In short, this command reads a list of servers from the "confluence_servers.txt" file, accesses a specific page on each server, and checks whether the page contains a string indicating the CVE-2021-26084 vulnerability. Based on this check, it prints "Vulnerable" in red for vulnerable servers and "OK" in green for non-vulnerable servers. It is a way to mass scan multiple Confluence servers for the presence of this vulnerability.

-----------------------------------------------------------------------------------------------------------------------------------------
18- 2021/CVE-2021-3129.json ???
(https://github.com//MadExploits//Laravel-debug-Checker) 

This code is very complex and I don't really understand what this code is doing. So, because of that i cant say if its a PoC or a Checker.
The only information about it is a site that is at README that tells “How to exploit a Remote Code Execution vulnerability in Laravel (CVE-2021-3129)”. This could be a clue as to what the code does but without being sure I can't say.
Link:
https://pentest-tools.com/blog/exploit-rce-vulnerability-laravel-cve-2021-3129 

-----------------------------------------------------------------------------------------------------------------------------------------
19- 2020/CVE-2020-14882.json Checker
(https://github.com//ovProphet//CVE-2020-14882-checker) 

The code you provided only checks whether the WebLogic server is vulnerable to a specific exploit, but does not perform any actual exploits. Therefore, it is more appropriate to classify it as a "checker".

The code does the following:

1- It defines a check function that takes an IP address, a port, and an SSL flag as arguments. 

2- The function constructs URLs for the WebLogic server with and without SSL based on the arguments provided.

3- It attempts to make an HTTP request to the WebLogic server and extract a cookie from the response.

4- It then makes several additional requests to try to exploit the vulnerability. Exploitation of the vulnerability involves running MVEL code on the WebLogic server to stop it and see if it responds with "Vuln host" in a 200 response code.

5- If the response contains "Vuln host" and the response code is 200 on one of the attempts, the function returns True, indicating that the server is vulnerable. Otherwise, it returns False.

6- The main function parses the command line arguments to obtain the IP addresses, port, and SSL flag, and then calls the check function for each IP address in the list.

7- If a server is found to be vulnerable, it is printed to standard output.

In short, this code is designed to check vulnerability in Oracle WebLogic servers that can be exploited for unauthorized remote code execution.

35- 2017/CVE-2017-9841.json ???
(https://github.com//MadExploits//PHPunit-Exploit) 

This code as the example of 37 is code is very complex and I don't really understand what this code is doing. So, because of that i cant say if its a PoC or a Checker.
The README tells “PHPUnit is a unit test framework for the PHP programming language. This is a sample xUnit architecture for a unit testing framework that originated with SUnit and became popular with JUnit. PHPUnit was created by Sebastian Bergmann”. This could be a clue as to what the code does but without being sure I can't say.

-----------------------------------------------------------------------------------------------------------------------------------------
20- 2021/CVE-2021-33560.json Checker
(https://github.com//IBM//PGP-client-checker-CVE-2021-33560) 

This code is a Python program that aims to check whether an OpenPGP client is vulnerable to a specific vulnerability (CVE-2021-33560) related to the size of the ephemeral secret in a Diffie-Hellman key exchange.

Here's a summary of how the code works:

1- It reads an OpenPGP message from the client. This can be done in two ways: by providing a file name as a command line argument or by reading standard input.

2- The code checks whether the OpenPGP message is not in ASCII armor format or not. If you don't have armor format, it will decode it to get the encrypted part.

3- It then looks for ElGamal cipher suites in the message, which are used in the Diffie-Hellman key exchange.

4- The code extracts the relevant components from these packages, such as the ephemeral keys (c0 and c1).

5- It then calculates the size of the ephemeral secret and checks whether it falls within a specific range.

6- Depending on the size of the ephemeral secret, it determines whether or not the client is vulnerable to CVE-2021-33560. If the size is within a certain range, it considers the client vulnerable.

7- It prints a message decreasing whether or not the client is affected by the vulnerability.

The code does this to check whether an OpenPGP client is vulnerable to a vulnerability that affects the size of the ephemeral secret used in Diffie-Hellman key exchanges. It is used to assess whether the client needs to be updated to a more secure version that fixes this specific vulnerability. In short it's a checker.

-----------------------------------------------------------------------------------------------------------------------------------------
21- 2019/CVE-2019-0708.json Checker
(https://github.com//davidfortytwo//bluekeep) 

This Python code is a vulnerability scanning utility that checks whether a set of target IP addresses is vulnerable to the vulnerability known as "BlueKeep". The BlueKeep vulnerability is a remote code execution vulnerability that affects Windows systems, specifically Remote Desktop (RDP) functionality.

Here's a brief explanation of what the code does:

1- Imports the necessary modules such as argparse, socket, ThreadPoolExecutor and as_completed.

2- Defines a function called check_bluekeep_vuln(target_ip) that checks whether a given target IP address is vulnerable to the BlueKeep vulnerability. The function performs the following:

>Attempts to establish a connection to the destination IP address on RDP port (3389).
>Sends a specific packet to the RDP service.
>Reads the response from the RDP service.
>If the response contains the pattern "\x03\x00\x00\x0c", the code considers the target as potentially VULNERABLE to BlueKeep and prints a corresponding message.
>Otherwise, the target is considered to be probably patched, and a corresponding message is printed. 

3- Defines a function called scan_ips(targets) that creates a pool of threads to execute the check_bluekeep_vuln() function in parallel for all target IP addresses specified in the targets list.

4- The main code checks that the script is running as a main program (and not being imported as a module), and then parses the command line arguments to get the list of targets to check.

5- It then calls the scan_ips() function with the target list provided on the command line and prints the results.

The code checks whether each target IP address is vulnerable to BlueKeep and provides information about the vulnerability status for each target. It is a useful tool for quickly checking which systems may be at risk of exploitation via this specific vulnerability. In short it a checker.

-----------------------------------------------------------------------------------------------------------------------------------------
22- 2021/CVE-2021-21985.json Checker
(https://github.com//onSec-fr//CVE-2021-21985-Checker)   

This PowerShell code performs the following actions:

1- It takes a command line argument, which must be a URL, and stores that URL in the $url variable.

2- Defines a set of custom HTTP headers in the $headers variable. These headers include information such as the "Host", "User-Agent", and "Content-Type" that will be used in the subsequent HTTP request.

3- Assembles a JSON request body in the $body variable. This request body contains a JSON object with a field called "methodInput". This object is used to send a request to a specific URL in JSON format.

4- Configures the [System.Net.ServicePointManager]::ServerCertificateValidationCallback variable to accept all server certificates, skipping SSL certificate validation. This may be necessary when working with servers with self-signed or untrusted certificates.

5- Makes an HTTP POST request to the URL "https://$url/ui/h5-vsan/rest/proxy/service/com.vmware.vsan.client.services.capability.VsanCapabilityProvider/getClusterCapabilityData" using the headers and body of request defined previously.

6- Converts the request response to JSON format using ConvertTo-Json.

7- Checks whether the JSON response contains the "result" keyword. If this keyword is present in the response, the code prints "TARGET VULNERABLE" in red. Otherwise it prints "TARGET NOT VULNERABLE" in green.

Basically, the code is used to check whether a given URL has a specific vulnerability. If the HTTP request response contains the word "result", the target is considered to be vulnerable; otherwise, it is considered non-vulnerable. This code can be useful in security testing and checking for vulnerabilities in specific URLs. In short it’s a checker.

-----------------------------------------------------------------------------------------------------------------------------------------
23- 2022/CVE-2022-4063.json Checker
(https://github.com//im-hanzou//INPGer) 

The provided code exploits the CVE-2022-4063 vulnerability in InPost Gallery through an LFI (Local File Inclusion) exploit that can lead to RCE (Remote Code Execution). 

Let's analyze the code to understand how it does this:

1- The code starts by defining the target URL and the command you want to run on the target server.

2- It then creates a payload that exploits the vulnerability. The payload is base64 encoded and contains a sequence of PHP filters that transform the original request so that it is executed as PHP code on the target server.

3- The payload is inserted into an HTTP GET request to the destination URL. The payload is passed as a parameter in an AJAX request to the admin-ajax.php file in the site's wp-admin directory.

4- The target server receives the request and processes the payload. Due to the LFI vulnerability, the server interprets the request as a malicious PHP command and executes it in the server context.

5- The output of executing the malicious PHP code is then returned as a response to the AJAX request.

6- The response is decoded from the original base64 format and is displayed in the program output.

The malicious PHP code contained in the payload is responsible for exploiting the LFI vulnerability in InPost Gallery and executing the desired command on the target server. This could allow an attacker to execute arbitrary code on the server, which is an RCE exploit. Therefore, the code demonstrates how the vulnerability can be exploited to execute remote code on the affected server. In short, these are malicious codes because they exploit the vulnerability itself, they not only check whether a server is vulnerable or not.

-----------------------------------------------------------------------------------------------------------------------------------------
24- 2023/CVE-2023-43654.json Checker
(https://github.com//OligoCyberSecurity//ShellTorchChecker) 

This code is a script designed to check for the presence of a specific vulnerability in a TorchServe instance. It is neither a Proof of Concept (PoC) nor an exploitation tool; rather, it serves as a checker to determine if the target TorchServe instance is vulnerable to a particular security issue.
Here's an overview of what the script does:

1- It performs pre-checks to determine whether the TorchServe instance is running locally (on the same machine as the script) or remotely (on a different machine).

2- It checks if the TorchServe management interface API is misconfigured. Specifically, it checks if the management interface is accessible remotely on a specified port (8081 by default) and reports whether it's open to remote connections.

3- It tests for the presence of the CVE-2023-43654 vulnerability, a Remote Server-Side Request Forgery (SSRF) issue. The script sends a POST request to the TorchServe instance to check if it can make arbitrary requests to a remote server and download a specific file. Depending on the response, it reports whether the vulnerability exists.

4- The script provides recommendations on how to mitigate the identified issues. For example, it suggests changing the configuration to limit the management interface to localhost only and configuring allowed URLs to prevent SSRF attacks.

In summary, this script is used to identify and report vulnerabilities related to TorchServe, providing information on whether specific security issues are present in the target instance. It does not exploit these vulnerabilities or perform any malicious actions. In short this is only a checker.

-----------------------------------------------------------------------------------------------------------------------------------------
25- 2022/CVE-2022-21449.json Checker
(https://github.com//Damok82//SignChecker) 

The provided code consists of two parts: a Java program (SignChecker.java) and a batch script (.bat file). These components work together to check for the vulnerability CVE-2022-21449 in different Java versions. Let's break down what each part does and whether they are a Proof of Concept (PoC) or a checker:
1- SignChecker.java:
This Java program is designed to demonstrate the vulnerability of CVE-2022-21449.
It generates an ECDSA key pair and performs digital signing and verification using the key pair.
The program accepts command-line arguments for a message and a signature and demonstrates the vulnerability by verifying the provided signature, even if it is incorrect.
It uses Java cryptographic functions to sign and verify messages.
The program can be seen as a Proof of Concept (PoC) because it showcases the vulnerability and how it can be exploited.
2- Batch Script:
The batch script is used to compile and run the Java program with different Java versions to test for the CVE-2022-21449 vulnerability.
It first checks the program's behavior with a patched version of Java (JDK 17.0.3) and then checks it with a vulnerable version of Java (JDK 17.0.2).
It sets the message and signature variables and then runs the Java program with these arguments.
The batch script can be seen as a checker because it tests whether the Java version is vulnerable to CVE-2022-21449. It does this by running the Java program with a given message and signature and checking the program's behavior.
In summary, the Java program (SignChecker.java) is a PoC that demonstrates the CVE-2022-21449 vulnerability, while the batch script is a checker that uses the PoC to test different Java versions for the vulnerability. Together, they provide a way to check whether a specific Java version is affected by the vulnerability. In short this is a checker.

-----------------------------------------------------------------------------------------------------------------------------------------
26- 2014/CVE-2014-0160.json Checker
(https://github.com//mozilla-services//Heartbleed) 

The provided code consists of multiple components that work together to create a Heartbleed test server and perform testing. Let's break down each part and determine whether they are a checker or a Proof of Concept (PoC):
1- main.go (Heartbleed Test Server):
This is the main Go source code for the Heartbleed test server.
It sets up an HTTP server that listens for incoming requests, handles caching, and communicates with the Heartbleed vulnerability-checking library.
The server can be used as a checker because it accepts incoming requests to test for the Heartbleed vulnerability and returns results.
2- config.json:
This JSON configuration file contains settings for the Heartbleed test server.
It defines various parameters such as access keys, DynamoDB configuration, and more.
It is not a checker or PoC on its own but rather provides configuration settings for the server.
build.sh (Shell Script):
This shell script is used to set up the Go environment, including setting the GOPATH and GOBIN.
It installs the Heartbleed test server and its dependencies.
The script is not a checker or PoC but rather a utility to prepare the environment for running the Heartbleed test server.
In summary:
The main.go file is the core of the Heartbleed test server and can be considered a checker because it handles incoming requests to test for the Heartbleed vulnerability.
The config.json file is not a checker or PoC but provides configuration settings for the server.
The build.sh script is not a checker or PoC but is used to set up the Go environment for running the server.
Together, these components create a Heartbleed vulnerability checker, allowing users to test for the Heartbleed vulnerability in SSL/TLS implementations. In short it it a Checker.


