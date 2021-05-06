# TEAMb
チームB



function myFunction() {

  sekine = 'sekine-kaho@webrage.jp';
  const recipient = sekine ;
  sub = 'google Apps Scriptによるメールテスト送信テスト'  
  const subject = sub ;

  const DOC_URL = 'https://docs.google.com/document/d/1yA6uyqI2tI57x9jS1idua3JhZnZ649dS1n77e4MBkF8/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);
  

　let options ={
    cc:sekine,
    bcc:sekine
};

scr = doc.getBody().getText();
let body = scr ;
GmailApp.sendEmail(recipient, subject, body, options);
}