# Github apiによるissue取得
## issue単体
```bash
$ curl https://api.github.com/repos/ivoryworks/til/issues/1
```
結果：
```json
{
  "url": "https://api.github.com/repos/ivoryworks/til/issues/1",
  "repository_url": "https://api.github.com/repos/ivoryworks/til",
  "labels_url": "https://api.github.com/repos/ivoryworks/til/issues/1/labels{/name}",
  "comments_url": "https://api.github.com/repos/ivoryworks/til/issues/1/comments",
  "events_url": "https://api.github.com/repos/ivoryworks/til/issues/1/events",
  "html_url": "https://github.com/ivoryworks/til/issues/1",
  "id": 269448227,
  "number": 1,
  "title": "Issue test",
  "user": {
    "login": "ivoryworks",
    "id": 839673,
    "avatar_url": "https://avatars3.githubusercontent.com/u/839673?v=4",
    "gravatar_id": "",
    "url": "https://api.github.com/users/ivoryworks",
    "html_url": "https://github.com/ivoryworks",
    "followers_url": "https://api.github.com/users/ivoryworks/followers",
    "following_url": "https://api.github.com/users/ivoryworks/following{/other_user}",
    "gists_url": "https://api.github.com/users/ivoryworks/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/ivoryworks/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/ivoryworks/subscriptions",
    "organizations_url": "https://api.github.com/users/ivoryworks/orgs",
    "repos_url": "https://api.github.com/users/ivoryworks/repos",
    "events_url": "https://api.github.com/users/ivoryworks/events{/privacy}",
    "received_events_url": "https://api.github.com/users/ivoryworks/received_events",
    "type": "User",
    "site_admin": false
  },
  "labels": [

  ],
  "state": "open",
  "locked": false,
  "assignee": null,
  "assignees": [

  ],
  "milestone": null,
  "comments": 0,
  "created_at": "2017-10-29T23:33:55Z",
  "updated_at": "2017-10-29T23:33:55Z",
  "closed_at": null,
  "author_association": "OWNER",
  "body": "ISSUE BODY.",
  "closed_by": null
}
```
## 配列
```bash
$ bash curl https://api.github.com/repos/ivoryworks/til/issues
```
結果：
```json
[
  {
    "url": "https://api.github.com/repos/ivoryworks/til/issues/2",
    "repository_url": "https://api.github.com/repos/ivoryworks/til",
    "labels_url": "https://api.github.com/repos/ivoryworks/til/issues/2/labels{/name}",
    "comments_url": "https://api.github.com/repos/ivoryworks/til/issues/2/comments",
    "events_url": "https://api.github.com/repos/ivoryworks/til/issues/2/events",
    "html_url": "https://github.com/ivoryworks/til/issues/2",
    "id": 269448433,
    "number": 2,
    "title": "Issue test 02",
    "user": {
      "login": "ivoryworks",
      "id": 839673,
      "avatar_url": "https://avatars3.githubusercontent.com/u/839673?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/ivoryworks",
      "html_url": "https://github.com/ivoryworks",
      "followers_url": "https://api.github.com/users/ivoryworks/followers",
      "following_url": "https://api.github.com/users/ivoryworks/following{/other_user}",
      "gists_url": "https://api.github.com/users/ivoryworks/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/ivoryworks/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/ivoryworks/subscriptions",
      "organizations_url": "https://api.github.com/users/ivoryworks/orgs",
      "repos_url": "https://api.github.com/users/ivoryworks/repos",
      "events_url": "https://api.github.com/users/ivoryworks/events{/privacy}",
      "received_events_url": "https://api.github.com/users/ivoryworks/received_events",
      "type": "User",
      "site_admin": false
    },
    "labels": [

    ],
    "state": "open",
    "locked": false,
    "assignee": null,
    "assignees": [

    ],
    "milestone": null,
    "comments": 0,
    "created_at": "2017-10-29T23:36:51Z",
    "updated_at": "2017-10-29T23:37:10Z",
    "closed_at": null,
    "author_association": "OWNER",
    "body": "Issue text."
  },
  {
    "url": "https://api.github.com/repos/ivoryworks/til/issues/1",
    "repository_url": "https://api.github.com/repos/ivoryworks/til",
    "labels_url": "https://api.github.com/repos/ivoryworks/til/issues/1/labels{/name}",
    "comments_url": "https://api.github.com/repos/ivoryworks/til/issues/1/comments",
    "events_url": "https://api.github.com/repos/ivoryworks/til/issues/1/events",
    "html_url": "https://github.com/ivoryworks/til/issues/1",
    "id": 269448227,
    "number": 1,
    "title": "Issue test 01",
    "user": {
      "login": "ivoryworks",
      "id": 839673,
      "avatar_url": "https://avatars3.githubusercontent.com/u/839673?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/ivoryworks",
      "html_url": "https://github.com/ivoryworks",
      "followers_url": "https://api.github.com/users/ivoryworks/followers",
      "following_url": "https://api.github.com/users/ivoryworks/following{/other_user}",
      "gists_url": "https://api.github.com/users/ivoryworks/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/ivoryworks/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/ivoryworks/subscriptions",
      "organizations_url": "https://api.github.com/users/ivoryworks/orgs",
      "repos_url": "https://api.github.com/users/ivoryworks/repos",
      "events_url": "https://api.github.com/users/ivoryworks/events{/privacy}",
      "received_events_url": "https://api.github.com/users/ivoryworks/received_events",
      "type": "User",
      "site_admin": false
    },
    "labels": [

    ],
    "state": "open",
    "locked": false,
    "assignee": null,
    "assignees": [

    ],
    "milestone": null,
    "comments": 0,
    "created_at": "2017-10-29T23:33:55Z",
    "updated_at": "2017-10-29T23:36:40Z",
    "closed_at": null,
    "author_association": "OWNER",
    "body": "ISSUE BODY."
  }
]
```
