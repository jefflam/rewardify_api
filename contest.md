# Contest Model

This is the model for contests on Rewardify.

---

### View all contests on Rewardify
#### [GET] /contests
Get request shortcut to view all contests on Rewardify. Probably will remove during production.

Response:
`
response = [
  {
    id: int,
    title: string,
    startDate: date,
    startTime: time,
    endDate: date,
    endTime: time,
    timeZone: string,
    entryRequirements: string,
    leaderboardDisplay: boolean,
    promotionMethodLikeFacebookPage: boolean,
    promotionMethodLikeFacebookPageUrl: string,
    promotionMethodTweet: boolean,
    promotionMethodTweetMessage: string,
    promotionMethodShareOnFacebook: boolean,
    promotionMethodShareOnFacebookMessage: string,
    promotionMethodInviteFacebookFriends: boolean,
    promotionMethodReferredFacebookFriend: boolean,
    rules: string,
    preContestPageCoverDesign: string,
    preContestPageCoverDesignText: string,
    preContestPageCoverDesignImage
    preContestPageCoverDesignHTML: string,
    contestPageCoverDesign: string,
    contestPageCoverDesignText: string,
    contestPageCoverDesignImage: string,
    contestPageCoverDesignHTML: string,
    postContestPageCoverDesign: string,
    postContestPageCoverDesignText: string,
    postContestPageCoverDesignImage: string,
    postContestPageCoverDesignHTML: string,
    uniqueContestId: string,
    owner: object
    participants: [
      // objects of participants
    ]
  }
]
`

---

### Create a new contest on Rewardify
#### [POST] /contest
Creating a new contest on Rewardify, and upon successful request will return back the contest information.

Request:
`
{
  title: string,
  startDate: date,
  startTime: time,
  endDate: date,
  endTime: time,
  timeZone: string,
  entryRequirements: string,
  leaderboardDisplay: boolean,
  promotionMethodLikeFacebookPage: boolean,
  promotionMethodLikeFacebookPageUrl: string,
  promotionMethodTweet: boolean,
  promotionMethodTweetMessage: string,
  promotionMethodShareOnFacebook: boolean,
  promotionMethodShareOnFacebookMessage: string,
  promotionMethodInviteFacebookFriends: boolean,
  promotionMethodReferredFacebookFriend: boolean,
  rules: string,
  preContestPageCoverDesign: string,
  preContestPageCoverDesignText: string,
  preContestPageCoverDesignImage
  preContestPageCoverDesignHTML: string,
  contestPageCoverDesign: string,
  contestPageCoverDesignText: string,
  contestPageCoverDesignImage: string,
  contestPageCoverDesignHTML: string,
  postContestPageCoverDesign: string,
  postContestPageCoverDesignText: string,
  postContestPageCoverDesignImage: string,
  postContestPageCoverDesignHTML: string,
  uniqueContestId: string,
  owner: object
}
`

Response:
`
response = [
  {
    id: int,
    title: string,
    startDate: date,
    startTime: time,
    endDate: date,
    endTime: time,
    timeZone: string,
    entryRequirements: string,
    leaderboardDisplay: boolean,
    promotionMethodLikeFacebookPage: boolean,
    promotionMethodLikeFacebookPageUrl: string,
    promotionMethodTweet: boolean,
    promotionMethodTweetMessage: string,
    promotionMethodShareOnFacebook: boolean,
    promotionMethodShareOnFacebookMessage: string,
    promotionMethodInviteFacebookFriends: boolean,
    promotionMethodReferredFacebookFriend: boolean,
    rules: string,
    preContestPageCoverDesign: string,
    preContestPageCoverDesignText: string,
    preContestPageCoverDesignImage
    preContestPageCoverDesignHTML: string,
    contestPageCoverDesign: string,
    contestPageCoverDesignText: string,
    contestPageCoverDesignImage: string,
    contestPageCoverDesignHTML: string,
    postContestPageCoverDesign: string,
    postContestPageCoverDesignText: string,
    postContestPageCoverDesignImage: string,
    postContestPageCoverDesignHTML: string,
    uniqueContestId: string,
    owner: object
    participants: [
      // objects of participants
    ]
  }
]
`

---

### Updating a contest's settings on Rewardify
#### [PUT] /contest/:id
Updating a user's account settings and upon successful request will return back the updated user account information.

Request:
`
{
  title: string,
  startDate: date,
  startTime: time,
  endDate: date,
  endTime: time,
  timeZone: string,
  entryRequirements: string,
  leaderboardDisplay: boolean,
  promotionMethodLikeFacebookPage: boolean,
  promotionMethodLikeFacebookPageUrl: string,
  promotionMethodTweet: boolean,
  promotionMethodTweetMessage: string,
  promotionMethodShareOnFacebook: boolean,
  promotionMethodShareOnFacebookMessage: string,
  promotionMethodInviteFacebookFriends: boolean,
  promotionMethodReferredFacebookFriend: boolean,
  rules: string,
  preContestPageCoverDesign: string,
  preContestPageCoverDesignText: string,
  preContestPageCoverDesignImage
  preContestPageCoverDesignHTML: string,
  contestPageCoverDesign: string,
  contestPageCoverDesignText: string,
  contestPageCoverDesignImage: string,
  contestPageCoverDesignHTML: string,
  postContestPageCoverDesign: string,
  postContestPageCoverDesignText: string,
  postContestPageCoverDesignImage: string,
  postContestPageCoverDesignHTML: string,
  uniqueContestId: string,
  owner: object
}
`

Response:
`
response = [
  {
    id: int,
    title: string,
    startDate: date,
    startTime: time,
    endDate: date,
    endTime: time,
    timeZone: string,
    entryRequirements: string,
    leaderboardDisplay: boolean,
    promotionMethodLikeFacebookPage: boolean,
    promotionMethodLikeFacebookPageUrl: string,
    promotionMethodTweet: boolean,
    promotionMethodTweetMessage: string,
    promotionMethodShareOnFacebook: boolean,
    promotionMethodShareOnFacebookMessage: string,
    promotionMethodInviteFacebookFriends: boolean,
    promotionMethodReferredFacebookFriend: boolean,
    rules: string,
    preContestPageCoverDesign: string,
    preContestPageCoverDesignText: string,
    preContestPageCoverDesignImage
    preContestPageCoverDesignHTML: string,
    contestPageCoverDesign: string,
    contestPageCoverDesignText: string,
    contestPageCoverDesignImage: string,
    contestPageCoverDesignHTML: string,
    postContestPageCoverDesign: string,
    postContestPageCoverDesignText: string,
    postContestPageCoverDesignImage: string,
    postContestPageCoverDesignHTML: string,
    uniqueContestId: string,
    owner: object
    participants: [
      // objects of participants
    ]
  }
]
`

---

### A new user participating in a contest
#### [PUT] /contest/:id/participate
Sending a PUT request to the specific contest with user information.
If it is a new user that does not have a Rewardify account, we create a new Rewardify user account first, receive the response with the user id, and then proceed with this request to participate (to be handled by the front-end probably).
Response for this request would be the participant's userId, email, ranking and score. Ranking can be '???' if the contest has displayLeaderboard as false.

Request:
`
{
  userId: int
}
`

Response:
`
response = {
  userId: int,
  email: string,
  ranking: string,
  score: string
}
`

---

### A contest participant promoting the contest
#### [PUT] /contest/:id/promotion
Sending a PUT request to the specific contest with the promotion type.
On the back-end, we should ensure that the user is not able to repeat the promotion again for certain promotiosn.
Response for this request would be the participant's userId, email, ranking, score and promotionType.
Ranking can be '???' if the contest has displayLeaderboard as false.
PromotionType would be a string indicating what promotion type the participant just did, and to update the front-end to prevent the user from being able to re-do the same promotion type if applicable.

Request:
`
{
  userId: int,
  promotionType: string
}
`

Response:
`
response = {
  userId: int,
  email: string,
  ranking: string,
  score: string,
  promotionType: string
}
`

---