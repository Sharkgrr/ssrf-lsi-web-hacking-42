# SSRF (Server-Side Request Forgery)

The attacker is able to make requests on behalf of the server, exploiting the server's capability to communicate with other servers, resources within the internal network and abusing server functionality to access or modify resources.

Types of SSRF

i. The one which displays response to attacker (Basic)

ii. The one which does not display response (Blind)

# LFI (Local File Inclusion)
Intent to exposing or running files on the web server. An LFI attack may lead to information disclosure, remote code execution, or even Cross-site Scripting (XSS). Typically, LFI occurs when an application uses the path to a file as input. 

## Scenarios / Testing 

1. Fetching: file:///etc/passwd

2. Fetching himself: http://0.0.0.0:5000

3. Exploit images: https://example.com/index.php?page=about.html

4. Example of reset password:
https://example.com/reset.php?token=n61jqwfkzwn99qjerjvwz0dn0tmn4bogu8sp5mmm

Access log file: /var/log/nginx/access.log

Monitoring the log:
```
172.17.0.1 - - [07/Apr/2023:13:58:59 +0000] "GET /reset.php?token=n61jqwfkzwn99qjerjvwz0dn0tmn4bogu8sp5mmm HTTP/1.1" 200 0 "-" "curl/7.85.0" "-"
```
5. Exploring visually directly on url: file:///

# More

Some attackers use Gopher Protocol.

The Gopher Protocol uses hierarchical menus and item selections to navigate servers. Gopher servers store information in plain text format, organized into directories and subdirectories. Users can browse these directories and select the items they wish to view.

# References

https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/07-Input_Validation_Testing/11.1-Testing_for_Local_File_Inclusion

https://www.acunetix.com/blog/articles/local-file-inclusion-lfi/

https://napoleon.com.br/glossario/o-que-e-gopher-protocol-2/

https://www.softwall.com.br/blog/ssrf-aws-uma-combinacao-perigosa/

https://medium.com/@madrobot/ssrf-server-side-request-forgery-types-and-ways-to-exploit-it-part-1-29d034c27978

https://medium.com/@Aptive/local-file-inclusion-lfi-web-application-penetration-testing-cc9dc8dd3601

https://portswigger.net/web-security/ssrf/blind