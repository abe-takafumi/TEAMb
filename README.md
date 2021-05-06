function myFunction() {
　
　yabuki = 'yabuki-tomohiko@webrage.jp';
　const recipient = yabuki ; 
  sub = 'Google Apps Scriptによるメール送信テスト';
  const subject = sub ;

  const DOC_URL = 'https://docs.google.com/document/d/1CQEP5K_UaPA3b13U9bi0YJ2Xtyhqyobenk84ZYXv520/edit';
  const doc = DocumentApp.openByUrl(DOC_URL) ;

  let options = {
    cc:yabuki,
    bcc:yabuki
  };
 
  scr = doc.getBody().getText();

  let body = scr ;

  GmailApp.sendEmail(recipient,subject,body,options);

}