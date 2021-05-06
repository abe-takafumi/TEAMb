# TEAMb
チームB



function myFunction() {
　const recipient = 'sekine-kaho@webrage.jp';   
  const subject = 'Google Apps Scriptによるメール送信テスト';

  const DOC_URL = 'https://docs.google.com/document/d/1yA6uyqI2tI57x9jS1idua3JhZnZ649dS1n77e4MBkF8/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);
  console.log(doc.getName());
  console.log(doc.getBody().getText());

  const recipientCompany = '株式会社ウェブレッジ';
  const recipientName = '関根花歩';

　let options ={
    cc:"sekine-kaho@webrege.jp"
};

let body = doc.getBody().getText();
GmailApp.sendEmail(recipient, subject, body, options);
}
