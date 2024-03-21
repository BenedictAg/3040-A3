# 3040Crypto
For 3040Crypto to prosper, implementing an API is necessary. Our API serves three basic requests essential for integration with external applications such as online shops and cryptocurrency exchange services. One of such requests is the ability to get a user's information by their user id. This allows external parties to view the details of a user such as their name and balance in order to detect if the account matches the customer that they are serving, or if they have sufficient funds. The second available request is modifying a user's wallet to either add or reduce funds. Finally, the last available request is creating a user account. This can encourage external services to lead their users without a crypto wallet to creating an account with 3040Crypto. Overall, the API we created places an emphasis on connectivity with services that benefit from accessing data directly from 3040Crypto.

<br />

### Resource
For more information on how to create API requests and the sample return values given, I encourage you to check [this](https://anvilproject.org/guides/content/creating-links) article on API examples.


# Endpoints
GET https://3040Crypto.com/accounts/id

PUT https://3040Crypto.com/amount?newAmount=amount

POST https://3040Crypto.com/accountcreation?first=str1&last=str2&balance=amount
