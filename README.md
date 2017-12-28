# System.Net.Mail

## General mail setting
MailAddress sender_mail = new MailAddress("sender_mail");//enter sender's email

MailMessage mail = new MailMessage();  

mail.To.Add("receiver_mail");//enter receiver's email

mail.From = sender_mail;

mail.Subject = "subject";  

mail.Body = "body"; 

mail.IsBodyHtml = false;


## Gmail
SmtpClient smtp = new SmtpClient();

smtp.Host = "smtp.gmail.com";

smtp.Port = 587;  

smtp.UseDefaultCredentials = false; 

smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

smtp.EnableSsl = true;

smtp.Send(mail);

## 126 mail
SmtpClient smtp = new SmtpClient();

smtp.Host = "smtp.126.com"; 

smtp.Port = 465; 

smtp.UseDefaultCredentials = false;  

smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

smtp.EnableSsl = true;

smtp.Send(mail);

## QQ mail
SmtpClient smtp = new SmtpClient(); 

smtp.Host = "smtp.qq.com";

smtp.Port = 587;  

smtp.UseDefaultCredentials = false;  

smtp.Credentials = new System.Net.NetworkCredential("sender_mail", "password"); // Enter sender's email and password 

smtp.EnableSsl = true;

smtp.Send(mail);

## Hotmail



####Reference:
1. https://msdn.microsoft.com/en-us/library/system.net.mail.mailmessage(v=vs.110).aspx
