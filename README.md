# Twitter

**User Table**

| Column   | Type    |
| -------- | ------- |
| user_id  | INTEGER |
| name     | TEXT    |
| username | TEXT    |
| password | TEXT    |
| gender   | TEXT    |

**Follower Table**

| Column              | Type    |
| ------------------- | ------- |
| `follower_id`       | INTEGER |
| `follower_user_id`  | INTEGER |
| `following_user_id` | INTEGER |

Here, if user1 follows user2 then,

`follower_user_id` is the user ID of user1 and `following_user_id` is the user ID of user2.

**Tweet Table**

| Column    | Type     |
| --------- | -------- |
| tweet_id  | INTEGER  |
| tweet     | TEXT     |
| user_id   | INTEGER  |
| date_time | DATETIME |

**Reply Table**

| Column    | Type     |
| --------- | -------- |
| reply_id  | INTEGER  |
| tweet_id  | INTEGER  |
| reply     | TEXT     |
| user_id   | INTEGER  |
| date_time | DATETIME |

**Like Table**

| Column    | Type     |
| --------- | -------- |
| like_id   | INTEGER  |
| tweet_id  | INTEGER  |
| user_id   | INTEGER  |
| date_time | DATETIME |

#### Sample Valid User Credentials

```
{
  "username":"JoeBiden",
  "password":"biden@123"
}
```

<Section id="section1" >

### API 1

#### Path: `/register/`

#### Method: `POST`

**Request**

```
{
  "username": "adam_richard",
  "password": "richard_567",
  "name": "Adam Richard",
  "gender": "male"
}


</Section>

<Section id="section2">

### API 2

#### Path: `/login/`

#### Method: `POST`

**Request**

```
{
  "username":"JoeBiden",
  "password":"biden@123"
}


</Section>

<Section id="authToken">

### Authentication with JWT Token

A middleware to authenticate the JWT token.


</Section>

<Section id="section3">

### API 3

#### Path: `/user/tweets/feed/`

#### Method: `GET`

#### Description:

Returns the latest tweets of people whom the user follows. Return 4 tweets at a time


</Section>

<Section id="section4">

### API 4

#### Path: `/user/following/`

#### Method: `GET`

#### Description:

Returns the list of all names of people whom the user follows


</Section>

<Section id="section5">

### API 5

#### Path: `/user/followers/`

#### Method: `GET`

#### Description:

Returns the list of all names of people who follows the user

<Section id="section6">

### API 6

#### Path: `/tweets/:tweetId/`

#### Method: `GET`


</Section>

<Section id="section7">

### API 7

#### Path: `/tweets/:tweetId/likes/`

#### Method: `GET`

</Section>

<Section id="section8">

### API 8

#### Path: `/tweets/:tweetId/replies/`

#### Method: `GET`


    </Section>

<Section id="section9">

### API 9

#### Path: `/user/tweets/`

#### Method: `GET`

#### Description:

Returns a list of all tweets of the user


</Section>

<Section id="section10">

### API 10

#### Path: `/user/tweets/`

#### Method: `POST`

#### Description:

Create a tweet in the tweet table

</Section>

<Section id="section11">

### API 11

#### Path: `/tweets/:tweetId/`

#### Method: `DELETE`


</Section>

<br/>

Use `npm install` to install the packages.
