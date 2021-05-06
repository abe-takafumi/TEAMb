# TEAMb
function myFunction() {

  abe = 'abe-takafumi@webrage.jp';
  const recipient = abe ;
  sub = 'Google Apps Scriptによるメール送信テスト';
  const subject = sub ;

  const DOC_URL = 'https://docs.google.com/document/d/1ZY82GtQuSE3ANs7ztfwMy_bDkqxyDt2ErlyekTofMTY/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);

  let options ={
    cc:abe,
    bcc:abe
  };

  scr = doc.getBody().getText();

  let body = scr ;
  
  GmailApp.sendEmail(recipient, subject, body, options);
}


