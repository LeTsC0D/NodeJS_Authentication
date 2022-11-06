![](Capture.PNG)
![](Capture1.PNG)
![](Capture2.PNG)
![](Capture3.PNG)
![](Capture4.PNG)

POST
http://localhost:3000/signup
raw , json  format
{
    "email":"shashank@gmail.com",
    "password":"shashank"
}

Output
{
    "_id": "63672bf9bf142f2a2476d4a8",
    "email": "shashank@gmail.com",
    "password": "$2a$10$DC7pfYc1LzJB72Y503TP7eoHG4X9WsKBQOvjLDt830Xe0dAvRJ4Ve",
    "createdAt": "2022-11-06T03:37:29.012Z",
    "updatedAt": "2022-11-06T03:37:29.012Z",
    "__v": 0
}


POST
http://localhost:3000/login
{
    "email":"shashank@gmail.com", 
    "password":"shashank"
}

Output
{
    "status": "ok",
    "data": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InNoYXNoYW5rQGdtYWlsLmNvbSIsInR5cGUiOiJ1c2VyIiwiaWF0IjoxNjY3NzA2Njg3fQ.mSpbxeLh3kdc0pFaDm6z0fmbfbPQilYNLWeWPq1Mz48"
}





GET (validity of token)
http://localhost:3000/
{
    "cookie": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InNoYXNoYW5rQGdtYWlsLmNvbSIsInR5cGUiOiJ1c2VyIiwiaWF0IjoxNjY3NzA2Njg3fQ.mSpbxeLh3kdc0pFaDm6z0fmbfbPQilYNLWeWPq1Mz48"
}

Output:
"valid token"


POST
http://localhost:3000/createAgencyClient

{
    "agentid": "3",
    "agentname":"shashancvgk21",
    "agentaddress1":"indiafdg121",
    "agentaddress2": "inddfgia121",
    "agentstate": "delhfdgi121",
    "agentcity":"delhi121",
    "agentphonenumber":"898738324124",
    "clientid":"3",
    "clientname":"srivadfgstava12",
    "clientemail":"shassdfgs121hank@gmail.com",
    "clientphonenumber":"898fg738324412",
    "clienttotalbill":"100134"
}

Output:
"account created"






PUT
http://localhost:3000/client/1
{
    "ClientId":"1",
    "Name":"name changed",
    "Email":"email changed",
    "PhoneNumber":"phone changed",
    "TotalBill":"1000"
}

Output
"the client has been updated"

GET
http://localhost:3000/maximum
Output
[
    {
        "_id": "6367670882e4b11138725ee9",
        "ClientId": "2",
        "AgencyId": "2",
        "Name": "srivastava12",
        "Email": "shas121hank@gmail.com",
        "PhoneNumber": "898738324412",
        "TotalBill": "100134",
        "createdAt": "2022-11-06T07:49:28.538Z",
        "updatedAt": "2022-11-06T07:49:28.538Z",
        "__v": 0
    },
    {
        "_id": "6367671d82e4b11138725eed",
        "ClientId": "3",
        "AgencyId": "3",
        "Name": "srivadfgstava12",
        "Email": "shassdfgs121hank@gmail.com",
        "PhoneNumber": "898fg738324412",
        "TotalBill": "100134",
        "createdAt": "2022-11-06T07:49:49.893Z",
        "updatedAt": "2022-11-06T07:49:49.893Z",
        "__v": 0
    }
]



