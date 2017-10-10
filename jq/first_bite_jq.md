# jqを試す
コマンドライン上でJSONをパースしてくれる人。
## install
```bash
$ brew install jq
```
## ただの整形
ex) github API
```bash
$ curl https://api.github.com | jq '.'
  % Total    % Received % Xferd  Average Speed   Time    Time    Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2165  100  2165    0     0    873      0  0:00:02  0:00:02 --:--:--   873
{
  "current_user_url": "https://api.github.com/user",
  "current_user_authorizations_html_url": "https://github.com/settings/connections/applications{/client_id}",
  "authorizations_url": "https://api.github.com/authorizations",
  "code_search_url": "https://api.github.com/search/code?q={query}{&page,per_page,sort,order}",
  "commit_search_url": "https://api.github.com/search/commits?q={query}{&page,per_page,sort,order}",
  "emails_url": "https://api.github.com/user/emails",
  "emojis_url": "https://api.github.com/emojis",
  "events_url": "https://api.github.com/events",
  "feeds_url": "https://api.github.com/feeds",
  "followers_url": "https://api.github.com/user/followers",
  "following_url": "https://api.github.com/user/following{/target}",
  "gists_url": "https://api.github.com/gists{/gist_id}",
  "hub_url": "https://api.github.com/hub",
  "issue_search_url": "https://api.github.com/search/issues?q={query}{&page,per_page,sort,order}",
  "issues_url": "https://api.github.com/issues",
  "keys_url": "https://api.github.com/user/keys",
  "notifications_url": "https://api.github.com/notifications",
  "organization_repositories_url": "https://api.github.com/orgs/{org}/repos{?type,page,per_page,sort}",
  "organization_url": "https://api.github.com/orgs/{org}",
  "public_gists_url": "https://api.github.com/gists/public",
  "rate_limit_url": "https://api.github.com/rate_limit",
  "repository_url": "https://api.github.com/repos/{owner}/{repo}",
  "repository_search_url": "https://api.github.com/search/repositories?q={query}{&page,per_page,sort,order}",
  "current_user_repositories_url": "https://api.github.com/user/repos{?type,page,per_page,sort}",
  "starred_url": "https://api.github.com/user/starred{/owner}{/repo}",
  "starred_gists_url": "https://api.github.com/gists/starred",
  "team_url": "https://api.github.com/teams",
  "user_url": "https://api.github.com/users/{user}",
  "user_organizations_url": "https://api.github.com/user/orgs",
  "user_repositories_url": "https://api.github.com/users/{user}/repos{?type,page,per_page,sort}",
  "user_search_url": "https://api.github.com/search/users?q={query}{&page,per_page,sort,order}"
}
```
## 配列で取り出す
```bash
$ curl https://api.github.com | jq '.[]'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2165  100  2165    0     0   2049      0  0:00:01  0:00:01 --:--:--  2050
"https://api.github.com/user"
"https://github.com/settings/connections/applications{/client_id}"
"https://api.github.com/authorizations"
"https://api.github.com/search/code?q={query}{&page,per_page,sort,order}"
"https://api.github.com/search/commits?q={query}{&page,per_page,sort,order}"
"https://api.github.com/user/emails"
"https://api.github.com/emojis"
"https://api.github.com/events"
"https://api.github.com/feeds"
"https://api.github.com/user/followers"
"https://api.github.com/user/following{/target}"
"https://api.github.com/gists{/gist_id}"
"https://api.github.com/hub"
"https://api.github.com/search/issues?q={query}{&page,per_page,sort,order}"
"https://api.github.com/issues"
"https://api.github.com/user/keys"
"https://api.github.com/notifications"
"https://api.github.com/orgs/{org}/repos{?type,page,per_page,sort}"
"https://api.github.com/orgs/{org}"
"https://api.github.com/gists/public"
"https://api.github.com/rate_limit"
"https://api.github.com/repos/{owner}/{repo}"
"https://api.github.com/search/repositories?q={query}{&page,per_page,sort,order}"
"https://api.github.com/user/repos{?type,page,per_page,sort}"
"https://api.github.com/user/starred{/owner}{/repo}"
"https://api.github.com/gists/starred"
"https://api.github.com/teams"
"https://api.github.com/users/{user}"
"https://api.github.com/user/orgs"
"https://api.github.com/users/{user}/repos{?type,page,per_page,sort}"
"https://api.github.com/search/users?q={query}{&page,per_page,sort,order}"
```
