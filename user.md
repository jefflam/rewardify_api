# User Model

This is the model for normal users or participants of contests on Rewardify.

---

### View all user accounts on Rewardify
#### [GET] /user
Get request shortcut to view all users on Rewardify. Probably will remove during production.

Response:
```
response = [
  {
    id: int,
    name: string,
    email: string,
    location: string,
    age: string,
    phone: string,
    photo: string,
    gender: string,
    facebook: string,
    contests: [
      // objects of contest models
    ]
  }
]
```

---

### Create a new user account on Rewardify
#### [POST] /user
Creating a new user on Rewardify, and upon successful request will return back the user account information.

Request:
```
{
  name: string,
  email: string,
  encryptedPassword: string,
  age: string,  // optional
  phone: string,  // optional
  photo: string,  // optional
  gender: string, // optional
  facebook": string // optional
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
    age: string,
    phone: string,
    photo: string,
    gender: string,
    facebook: string
  }
]
```

---

### Updating a user's settings on Rewardify
#### [PUT] /user/:id
Updating a user's account settings and upon successful request will return back the updated user account information.

Request:
```
{
  name: string,
  password: string,
  age: string,  // optional
  phone: string,  // optional
  photo: string,  // optional
  gender: string, // optional
  facebook": string // optional
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
    age: string,
    phone: string,
    photo: string,
    gender: string,
    facebook: string
  }
]
```
