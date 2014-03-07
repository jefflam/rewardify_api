# Business Model

This is the model for business accounts/users or creators of contests on Rewardify.

---

### View all user accounts on Rewardify
#### [GET] /business
Get request shortcut to view all businesses on Rewardify. Probably will remove during production.

Response:
```
response = [
  {
    id: int,
    name: string,
    email: string,
    location: string,
    company: string,
    phone: string,
    industry: string,
    photo: string,
    contests: [
      // objects of contest models
    ]
  }
]
```

---

### Create a new business account on Rewardify
#### [POST] /business
Creating a new business account on Rewardify, and upon successful request will return back the business account information.

Request:
```
{
  name: string,
  email: string,
  encryptedPassword: string
  location: string, // optional
  company: string, // optional
  phone: string, // optional
  industry: string, // optional
  photo: string // optional
}
```

Response:
```
response = [
  {
    id: int,
    name: string,
    email: string,
    location: string,
    company: string,
    phone: string,
    industry: string,
    photo: string
  }
]
```

---

### Updating a business's settings on Rewardify
#### [PUT] /business/:id
Updating a user's account settings and upon successful request will return back the updated user account information.

Request:
```
{
  "name": string,
  "password": string,
  "age": string,  // optional
  "phone": string,  // optional
  "photo": string,  // optional
  "gender": string, // optional
  "facebook": string // optional
}
```

Response:
```
response = [
  {
    id: int,
    "name": string,
    "password": string,
    "age": string,
    "phone": string,
    "photo": string,
    "gender": string,
    "facebook": string
  }
]
```

---

