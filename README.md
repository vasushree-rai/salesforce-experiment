# salesforce-experiment
using sales force for the first time
#Trying to send a mail using salesforce and showing an exec log
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/1f674261-3d19-4eaf-833a-11a48d3b1534" />
#Exec log
<img width="992" height="611" alt="image" src="https://github.com/user-attachments/assets/ec6e5617-5e6f-4ad3-8354-9d6c9d3bde2d" />
#the code used to execute 
// 1. Set up the email parameters
List<String> toAddresses = new List<String>{'vasushree.cs23@sahyadri.edu.in'};
String subject = 'Salesforce Apex Test Email';
String body = '<h1>Success!</h1><p>This email was successfully sent from Salesforce Apex code.</p>';

// 2. Create the email object
Messaging.SingleEmailMessage mail = new Messaging.SingleEmailMessage();
mail.setToAddresses(toAddresses);
mail.setSubject(subject);
mail.setHtmlBody(body);

// 3. Send it immediately (No rollback this time)
List<Messaging.Email> emails = new List<Messaging.Email>{mail};
List<Messaging.SendEmailResult> results = Messaging.sendEmail(emails);

// 4. Print confirmation to the log panel
for (Messaging.SendEmailResult result : results) {
    if (result.isSuccess()) {
        System.debug(LoggingLevel.ERROR, '✅ Email sent successfully to: ' + toAddresses[0]);
    } else {
        System.debug(LoggingLevel.ERROR, '❌ Failed to send email: ' + result.getErrors()[0].getMessage());
    }
}
