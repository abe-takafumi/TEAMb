# TEAMb
function myFunction() {

  rec_address = 'yabuki-tomohiko@webrage.jp,ishii-hiroto@webrage.jp,sekine-kaho@webrage.jp';
  cc_address = 'abe-takafumi@webrage.jp';
  bcc_address = 'abe-takafumi@webrage.jp';
  sub = 'Google Apps Scriptによるメール送信テスト';
  
  const DOC_URL = 'https://docs.google.com/document/d/1ZY82GtQuSE3ANs7ztfwMy_bDkqxyDt2ErlyekTofMTY/edit'; 
  const doc = DocumentApp.openByUrl(DOC_URL);
  scr = doc.getText();

  const recipient = rec_address;
  const subject = sub ;
  const body = scr ;
  const options ={
    cc:cc_address,
    bcc:bcc_address
  };
  
  GmailApp.sendEmail(recipient, subject, body, options);
}