# TEAMb
function myFunction() {

  let ishii = 'ishii-hiroto@webrage.jp';

  const recipient = ishii;
  
  sub ='GASによるメール送信テスト'
  const subject = sub

  const DOC_URL = 'https://docs.google.com/document/d/1yUx8oFtiow3cxlh-5BJC2wRZN1icI6Ia3IRtoRIzpRw/edit';
  const doc = DocumentApp.openByUrl(DOC_URL);

  let  options = {
  cc: ishii,
  bcc: ishii
  };

  let body = doc.getText();

  GmailApp.sendEmail(recipient,subject,body,options);

}