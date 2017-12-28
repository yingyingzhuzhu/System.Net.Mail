# System.Net.Mail

## General mail setting

*Write code as follows:*

    MailAddress sender_mail = new MailAddress("sender_mail");//enter sender's email

    MailMessage mail = new MailMessage();  

    mail.To.Add("receiver_mail");//enter receiver's email

    mail.From = sender_mail;

    mail.Subject = "subject";  

    mail.Body = "body"; 

    mail.IsBodyHtml = false;


## Gmail
*Manage Gmail account access as follows:*

1. Login to sender's Gmail account
2. Select "Sign-in & security"
![](https://www.dropbox.com/s/6eaz72xjm19jzsg/Sign-in_and_security.png?dl=0)
3. Select "Apps with account access"
![](https://www.dropbox.com/s/pttpum34h8qt50s/Gmail_apps_with_account_access.png?dl=0)
4. Set "Allow less secure apps" as "ON"
![](https://www.dropbox.com/s/pttpum34h8qt50s/Gmail_apps_with_account_access.png?dl=0)

*Write code as follows:*


    SmtpClient smtp = new SmtpClient();

    smtp.Host = "smtp.gmail.com";

    smtp.Port = 587;  

    smtp.UseDefaultCredentials = false; 

    smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

    smtp.EnableSsl = true;

    smtp.Send(mail);



## 126 mail
*Write code as follows:*

    SmtpClient smtp = new SmtpClient();

    smtp.Host = "smtp.126.com"; 

    smtp.Port = 465; 

    smtp.UseDefaultCredentials = false;  

    smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

    smtp.EnableSsl = true;

    smtp.Send(mail);

## QQ mail
*Write code as follows:*

    SmtpClient smtp = new SmtpClient(); 

    smtp.Host = "smtp.qq.com";

    smtp.Port = 587;  

    smtp.UseDefaultCredentials = false;  

    smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

    smtp.EnableSsl = true;

    smtp.Send(mail);

## Hotmail



Reference:
1. https://msdn.microsoft.com/en-us/library/system.net.mail.mailmessage(v=vs.110).aspx
