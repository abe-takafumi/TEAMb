# TEAMb
function myFunction() {

  const recipient = 'abe-takafumi@webrage.jp'; 
  const subject = 'Google Apps Scriptによるメール送信テスト';

  const DOC_URL = 'https://docs.google.com/document/d/1ZY82GtQuSE3ANs7ztfwMy_bDkqxyDt2ErlyekTofMTY/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);
  console.log(doc.getBody().getText());

  const recipientCompany = '株式会社ウェブレッジ';
  const recipientName = '阿部タカフミ';

  let options ={
    cc:"abe-takafumi@webrage.jp",
    bcc:"abe-takafumi@webrage.jp"
  };
  let body = doc.getBody().getText();
  
  
  GmailApp.sendEmail(recipient, subject, body, options);
}
