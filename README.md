# 3040Crypto
For 3040Crypto to prosper, implementing an API is necessary. Our API serves three basic requests essential for integration with external applications such as online shops and cryptocurrency exchange services. One of such requests is the ability to get a user's information by their user id. This allows external parties to view the details of a user such as their name and balance in order to detect if the account matches the customer that they are serving, or if they have sufficient funds. The second available request is modifying a user's wallet to either add or reduce funds. Finally, the last available request is creating a user account. This can encourage external services to lead their users without a crypto wallet to creating an account with 3040Crypto. Overall, the API we created places an emphasis on connectivity with services that benefit from accessing data directly from 3040Crypto.

<br />

### Resource
For more information on how to create API requests and the sample return values given, I encourage you to check [this](https://anvilproject.org/guides/content/creating-links) article on API examples.


# Endpoints
GET https://3040Crypto.com/accounts/id

PUT https://3040Crypto.com/accounts/id/amount?newAmount=amount

POST https://3040Crypto.com/accountcreation?first=str1&last=str2&balance=amount

# Sample Responses
curl https://3040Crypto.com/accounts/id

```
{
    "user_id": id,
    "first_name": "test",
    "last_name": "test",
    "balance": (int) value
    "status": "200 OK"
}
```

curl https://3040Crypto.com/accounts/id/amount?newAmount=amount
```
{
    "user_id": id,
    "name": "test test",
    "old_amount": 400000,
    "new_amount": amount,
    "total_amount": sum(400000, amount),
    "status": "200 OK"
}
```

curl https://3040Crypto.com/accountcreation?first=str1&last=str2&balance=amount

```
{
    "status": "200 OK"
}
```

# Sample Example

curl https://3040Crypto.com/accounts/4325
```
{
    "user_id": 4325,
    "first_name": "Sachin",
    "last_name": "Bhatt",
    "balance": 800000,
    "status": "200 OK"
}
```

curl https://3040Crypto.com/accounts/1234/amount?newAmount=54000
```
{
    "user_id": 1234,
    "name": "Sachin Bhatt",
    "old_amount": 400000,
    "new_amount": 54000,
    "total_amount": 454000,
    "status": "200 OK"
}
```

curl https://3040Crypto.com/accountcreation?first=Sachin&last=Bhatt&balance=1234567

```
{
    "status": "200 OK"
}
```
