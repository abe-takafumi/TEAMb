# TEAMb
function myFunction() {

  des = 'abe-takafumi@webrage.jp';
  sub = 'Google Apps Scriptによるメール送信テスト';
  
  const DOC_URL = 'https://docs.google.com/document/d/1ZY82GtQuSE3ANs7ztfwMy_bDkqxyDt2ErlyekTofMTY/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);
  scr = doc.getText();

  const recipient = des;
  const subject = sub ;
  const body = scr ;
  const options ={
    cc:des,
    bcc:des
  };
  
  GmailApp.sendEmail(recipient, subject, body, options);
}