# https-leetcode.com-test
Here is solution for https://leetcode.com/problems/unique-email-addresses/

```
    var numUniqueEmails = function(emails) {
    
    const callback = email => {
    const beforePlus = email.substr(0, email.indexOf('+'));
    const withoutDots = beforePlus.split('.').join("");
    const domain = email.substring(email.indexOf("@"));
    const result = withoutDots + domain;
    return result;
  }
  const mainIterator = emails.map(callback);
  const number = mainIterator.filter((x, i, a) => a.indexOf(x) == i).length;
    return number;
    
}; 
```
```
const emails = ["test.email+alex@leetcode.com","test.e.mail+bob.cathy@leetcode.com","testemail+david@lee.tcode.com"];
const emails = ["test.email+alex@leetcode.com","test.e.mail+bob.cathy@leetcode.com","testemail+david@lee.tcode.com"];
and etc
```
