# https-leetcode.com-test
Here is solution for https://leetcode.com/problems/unique-email-addresses/

```
var numUniqueEmails = function(emails) {
  const callback = email => {
      const localNames=email.substr(0, email.indexOf('@'));
      const trimmedLocalName=localNames.replace(/\+(.*)$/, '').replace(/\./g, '');
      const domain = email.substring(email.indexOf("@"));
      const result = trimmedLocalName + domain;
      return result;
    }
  const number = emails.map(callback).filter((x, i, a) => a.indexOf(x) == i).length;
    return number;
}; 

```
```
test: 
const emails = ['email@mighway.co', 'email+test@mighway.co']
const emails = ["test.email+alex@leetcode.com","test.e.mail+bob.cathy@leetcode.com","testemail+david@lee.tcode.com"];
and etc
```
