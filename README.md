# paper-data-nu-college-scheduler

# 🚀 Easily plan your years of courses at Northwestern University. 🚀

https://github.com/coding-to-music/paper-data-nu-college-scheduler

https://paper-data-nu-college-scheduler.vercel.app

From / By https://github.com/dilanx/paper.nu

https://www.paper.nu/?

## Environment variables:

```java
  const s3Client = new S3Client({
    endpoint: 'https://nyc3.digitaloceanspaces.com',
    region: 'nyc3',
    credentials: {
      accessKeyId: process.env.CDN_ACCESS_KEY,
      secretAccessKey: process.env.CDN_ACCESS_SECRET,

  await fetch(process.env.LOG_WEBHOOK, {

const SERVER = 'https://northwestern-prod.apigee.net';

export async function getTerms() {
  const response = await fetch(`${SERVER}/student-system-termget/UGRD`, {
    headers: { apikey: process.env.API_KEY },

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/paper-data-nu-college-scheduler.git
git push -u origin main
```

# paper.nu data automation

## Key mapping

To significantly reduce data size, repeated keys are shortened. For example, instead of 3000 courses each having a `description` property, they have a `d` property, thus resulting in 10 \* 3000 less characters in the file. This takes up less bandwidth when downloading from the CDN and less storaged when cached on the client. The client can map the data in reverse if necessary.

### Plan data

#### Majors

| Short | Long    |
| ----- | ------- |
| i     | id      |
| c     | color   |
| d     | display |

#### Courses

| Short | Long        |
| ----- | ----------- |
| i     | id          |
| n     | name        |
| u     | units       |
| r     | repeatable  |
| d     | description |
| p     | prereqs     |
| s     | distros     |
| l     | placeholder |

### Schedule data

#### Courses

| Short | Long      |
| ----- | --------- |
| i     | course_id |
| c     | school    |
| t     | title     |
| u     | subject   |
| n     | number    |
| s     | sections  |

#### Sections

| Short | Long         |
| ----- | ------------ |
| i     | section_id   |
| r     | instructors  |
| t     | title        |
| u     | subject      |
| n     | number       |
| s     | section      |
| m     | meeting_days |
| x     | start_time   |
| y     | end_time     |
| l     | room         |
| d     | start_date   |
| e     | end_date     |
| c     | component    |
| a     | capacity     |
| q     | enrl_req     |
| p     | descs        |
| o     | distros      |

#### Instructors

| Short | Long           |
| ----- | -------------- |
| n     | name           |
| p     | phone          |
| a     | campus_address |
| o     | office_hours   |
| b     | bio            |
| u     | url            |
