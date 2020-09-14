open file php.ini in C:\xampp\php

find and change the value to this :

[mail function]
For Win32 only.
http://php.net/smtp
SMTP=smtp.gmail.com
http://php.net/smtp-port
smtp_port=587
sendmail_from = your_email_address_here
sendmail_path = "\"C:\xampp\sendmail\sendmail.exe\" -t"

and then change file sendmail.ini in C:\xampp\sendmail

find and change the value to this :

smtp_server=smtp.gmail.com
smtp_port=587
error_logfile=error.log
debug_logfile=debug.log
auth_username=your_email_address_here
auth_password=your_password_here
force_sender=your_email_address_here (it's optional)

!!!WARNING!!!

1. MAKE SURE YOUR SENDER EMAIL HAS 2ND-VERIFICATION ACTIVATED
2. THEN CREATE APP PASSWORD AND SELECT "SELECT APP" TO OTHER CUSTOM NAME
3. THEN GENERATE
4. COPY AND PASTE TH GENERATED PASS TO "AUTH_PASSWORD =" IN sendmail.ini