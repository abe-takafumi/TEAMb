# TEAMb
チームB
function myFunction() {
  const recipient = 'yabuki-tomohiko@webrage.jp'; 
  const subject = 'Google Apps Scriptによるメール送信テスト';
  const DOC_URL = 'https://docs.google.com/document/d/1CQEP5K_UaPA3b13U9bi0YJ2Xtyhqyobenk84ZYXv520/edit';
  const doc = DocumentApp.openByUrl(DOC_URL) ;
  
  const recipientCompany = '株式会社ウェブレッジ';
  const recipientName = '矢吹知彦';
  
  let options = {
    cc:"yabuki-tomohiko@webrage.jp",
   bcc:"yabuki-tomohiko@webrage.jp"
  };
  let body = doc.getBody().getText();
  GmailApp.sendEmail(recipient,subject,body,options);

}