---
id: E4tHh7Kq6jlwGiNAjAJZO
title: Scalability
desc: ''
updated: 1643537071396
created: 1643534154250
---

If we increase the number of users or amount of data that passes through the system, how do we add additional computing power to cope with the load?

## Describing Load

- What are your system's _load parameters_? (e.g. DB read/write ratio, concurrent connections, bandwidth usage, whale users, etc.)

e.g. Twitter home page. 
- A user can follow many people. When user goes to home page, fetch all recent tweets of followees from DB. Problem: DB reads expensive.
- Solution: cache a user's home page. When followee tweets, update followers' caches. Problem: Celebrities have many followers. Tweets are expensive as they need to update millions of cache entries.
- Solution: Use both. Don't update cache for whale followees. If user follows a whale user, fetch from DB to get update from them.

## Describing Performance

