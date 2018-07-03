## Random Notes
- [OAuth](https://developer.github.com/v3/#authentication)
- [Pagination](https://developer.github.com/v3/#pagination)
    - Requests that return multiple items will be paginated to 30 items by default. You can specify further pages with the ?page parameter. For some resources, you can also set a custom page size up to 100 with the ?per_page parameter. Note that for technical reasons not all endpoints respect the ?per_page parameter, see events for example.
    - Note that page numbering is 1-based and that omitting the ?page parameter will return the first page.
    - [Traversing with Pagination Guide](https://developer.github.com/v3/guides/traversing-with-pagination/)

## GET User's Info by Username

**Summary**: Gets user's info 

**Required**: username

**Call**: GET `https://api.github.com/users/USERNAME` or GET `https://api.github.com/users/USERNAME?-H=Accept:%20application/vnd.github.v3.full+json`  

**Details**: Returns a JSON hash, with Strings as keys.

**Example**:  
```JSON
{
    "login": "USERNAME",
    "id": 42424242,
    "node_id": "FOO4BARlcjI2FOoyMbAz",
    "avatar_url": "https://avatars2.githubusercontent.com/u/77777752?v=4",
    "gravatar_id": "",
    "url": "https://api.github.com/users/USERNAME",
    "html_url": "https://github.com/USERNAME",
    "followers_url": "https://api.github.com/users/USERNAME/followers",
    "following_url": "https://api.github.com/users/USERNAME/following{/other_user}",
    "gists_url": "https://api.github.com/users/USERNAME/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/USERNAME/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/USERNAME/subscriptions",
    "organizations_url": "https://api.github.com/users/USERNAME/orgs",
    "repos_url": "https://api.github.com/users/USERNAME/repos",
    "events_url": "https://api.github.com/users/USERNAME/events{/privacy}",
    "received_events_url": "https://api.github.com/users/USERNAME/received_events",
    "type": "User",
    "site_admin": false,
    "name": "Ada Lovelace",
    "company": null,
    "blog": "",
    "location": "Seattle, WA",
    "email": null,
    "hireable": null,
    "bio": "Foo bar baz",
    "public_repos": 72,
    "public_gists": 2,
    "followers": 1,
    "following": 1,
    "created_at": "2017-06-04T06:46:11Z",
    "updated_at": "2018-04-16T23:55:08Z"
}
```

## GET Repo Details by Username

**Summary**: Gets detailed representation of an individual repository

**Required**: username and repo name

**Call**: GET `https://api.github.com/repos/octokit/REPONAME.rb?-H=Accept:%20application/vnd.github.v3.full+json`  

**Details**: returns a JSON hash, with Strings as keys.

**Example** 
````JSON
{
    "id": 417862,
    "node_id": "MDEwOlJlcG9zaXRvcnk0MTc4NjI=",
    "name": "REPONAME.rb",
    "full_name": "octokit/REPONAME.rb",
    "owner": {
        "login": "octokit",
        "id": 3430433,
        "node_id": "MDEyOk9yZ2FuaXphdGlvbjM0MzA0MzM=",
        "avatar_url": "https://avatars0.githubusercontent.com/u/3430433?v=4",
        "gravatar_id": "",
        "url": "https://api.github.com/users/octokit",
        "html_url": "https://github.com/octokit",
        "followers_url": "https://api.github.com/users/octokit/followers",
        "following_url": "https://api.github.com/users/octokit/following{/other_user}",
        "gists_url": "https://api.github.com/users/octokit/gists{/gist_id}",
        "starred_url": "https://api.github.com/users/octokit/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/octokit/subscriptions",
        "organizations_url": "https://api.github.com/users/octokit/orgs",
        "repos_url": "https://api.github.com/users/octokit/repos",
        "events_url": "https://api.github.com/users/octokit/events{/privacy}",
        "received_events_url": "https://api.github.com/users/octokit/received_events",
        "type": "Organization",
        "site_admin": false
    },
    "private": false,
    "html_url": "https://github.com/octokit/octokit.rb",
    "description": "Ruby toolkit for the GitHub API",
    "fork": false,
    "url": "https://api.github.com/repos/octokit/octokit.rb",
    "forks_url": "https://api.github.com/repos/octokit/octokit.rb/forks",
    "keys_url": "https://api.github.com/repos/octokit/octokit.rb/keys{/key_id}",
    "collaborators_url": "https://api.github.com/repos/octokit/octokit.rb/collaborators{/collaborator}",
    "teams_url": "https://api.github.com/repos/octokit/octokit.rb/teams",
    "hooks_url": "https://api.github.com/repos/octokit/octokit.rb/hooks",
    "issue_events_url": "https://api.github.com/repos/octokit/octokit.rb/issues/events{/number}",
    "events_url": "https://api.github.com/repos/octokit/octokit.rb/events",
    "assignees_url": "https://api.github.com/repos/octokit/octokit.rb/assignees{/user}",
    "branches_url": "https://api.github.com/repos/octokit/octokit.rb/branches{/branch}",
    "tags_url": "https://api.github.com/repos/octokit/octokit.rb/tags",
    "blobs_url": "https://api.github.com/repos/octokit/octokit.rb/git/blobs{/sha}",
    "git_tags_url": "https://api.github.com/repos/octokit/octokit.rb/git/tags{/sha}",
    "git_refs_url": "https://api.github.com/repos/octokit/octokit.rb/git/refs{/sha}",
    "trees_url": "https://api.github.com/repos/octokit/octokit.rb/git/trees{/sha}",
    "statuses_url": "https://api.github.com/repos/octokit/octokit.rb/statuses/{sha}",
    "languages_url": "https://api.github.com/repos/octokit/octokit.rb/languages",
    "stargazers_url": "https://api.github.com/repos/octokit/octokit.rb/stargazers",
    "contributors_url": "https://api.github.com/repos/octokit/octokit.rb/contributors",
    "subscribers_url": "https://api.github.com/repos/octokit/octokit.rb/subscribers",
    "subscription_url": "https://api.github.com/repos/octokit/octokit.rb/subscription",
    "commits_url": "https://api.github.com/repos/octokit/octokit.rb/commits{/sha}",
    "git_commits_url": "https://api.github.com/repos/octokit/octokit.rb/git/commits{/sha}",
    "comments_url": "https://api.github.com/repos/octokit/octokit.rb/comments{/number}",
    "issue_comment_url": "https://api.github.com/repos/octokit/octokit.rb/issues/comments{/number}",
    "contents_url": "https://api.github.com/repos/octokit/octokit.rb/contents/{+path}",
    "compare_url": "https://api.github.com/repos/octokit/octokit.rb/compare/{base}...{head}",
    "merges_url": "https://api.github.com/repos/octokit/octokit.rb/merges",
    "archive_url": "https://api.github.com/repos/octokit/octokit.rb/{archive_format}{/ref}",
    "downloads_url": "https://api.github.com/repos/octokit/octokit.rb/downloads",
    "issues_url": "https://api.github.com/repos/octokit/octokit.rb/issues{/number}",
    "pulls_url": "https://api.github.com/repos/octokit/octokit.rb/pulls{/number}",
    "milestones_url": "https://api.github.com/repos/octokit/octokit.rb/milestones{/number}",
    "notifications_url": "https://api.github.com/repos/octokit/octokit.rb/notifications{?since,all,participating}",
    "labels_url": "https://api.github.com/repos/octokit/octokit.rb/labels{/name}",
    "releases_url": "https://api.github.com/repos/octokit/octokit.rb/releases{/id}",
    "deployments_url": "https://api.github.com/repos/octokit/octokit.rb/deployments",
    "created_at": "2009-12-10T21:41:49Z",
    "updated_at": "2018-07-02T11:57:51Z",
    "pushed_at": "2018-06-26T21:36:13Z",
    "git_url": "git://github.com/octokit/octokit.rb.git",
    "ssh_url": "git@github.com:octokit/octokit.rb.git",
    "clone_url": "https://github.com/octokit/octokit.rb.git",
    "svn_url": "https://github.com/octokit/octokit.rb",
    "homepage": "http://octokit.github.io/octokit.rb/",
    "size": 13238,
    "stargazers_count": 2885,
    "watchers_count": 2885,
    "language": "Ruby",
    "has_issues": true,
    "has_projects": true,
    "has_downloads": true,
    "has_wiki": false,
    "has_pages": true,
    "forks_count": 860,
    "mirror_url": null,
    "archived": false,
    "open_issues_count": 25,
    "license": {
        "key": "mit",
        "name": "MIT License",
        "spdx_id": "MIT",
        "url": "https://api.github.com/licenses/mit",
        "node_id": "MDc6TGljZW5zZTEz"
    },
    "forks": 860,
    "open_issues": 25,
    "watchers": 2885,
    "default_branch": "master",
    "organization": {
        "login": "octokit",
        "id": 3430433,
        "node_id": "MDEyOk9yZ2FuaXphdGlvbjM0MzA0MzM=",
        "avatar_url": "https://avatars0.githubusercontent.com/u/3430433?v=4",
        "gravatar_id": "",
        "url": "https://api.github.com/users/octokit",
        "html_url": "https://github.com/octokit",
        "followers_url": "https://api.github.com/users/octokit/followers",
        "following_url": "https://api.github.com/users/octokit/following{/other_user}",
        "gists_url": "https://api.github.com/users/octokit/gists{/gist_id}",
        "starred_url": "https://api.github.com/users/octokit/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/octokit/subscriptions",
        "organizations_url": "https://api.github.com/users/octokit/orgs",
        "repos_url": "https://api.github.com/users/octokit/repos",
        "events_url": "https://api.github.com/users/octokit/events{/privacy}",
        "received_events_url": "https://api.github.com/users/octokit/received_events",
        "type": "Organization",
        "site_admin": false
    },
    "network_count": 860,
    "subscribers_count": 195
}
````

## GET Organization by Organization's Username 

**Summary**: Gets summary representation of each repos

**Call**: GET `https://api.github.com/orgs/Ada-Developers-Academy/repos?-H=Accept:%20application/vnd.github.v3.full+json`

**Details**: Returns an array of JSON hashes, with Strings as keys.

**Example** 
```JSON
[
    {
        "id": 10668530,
        "node_id": "MDEwOlJlcG9zaXRvcnkxMDY2ODUzMA==",
        "name": "LessonPlanning",
        "full_name": "Ada-Developers-Academy/LessonPlanning",
        "owner": {
            "login": "Ada-Developers-Academy",
            "id": 4689715,
            "node_id": "MDEyOk9yZ2FuaXphdGlvbjQ2ODk3MTU=",
            "avatar_url": "https://avatars2.githubusercontent.com/u/4689715?v=4",
            "gravatar_id": "",
            "url": "https://api.github.com/users/Ada-Developers-Academy",
            "html_url": "https://github.com/Ada-Developers-Academy",
            "followers_url": "https://api.github.com/users/Ada-Developers-Academy/followers",
            "following_url": "https://api.github.com/users/Ada-Developers-Academy/following{/other_user}",
            "gists_url": "https://api.github.com/users/Ada-Developers-Academy/gists{/gist_id}",
            "starred_url": "https://api.github.com/users/Ada-Developers-Academy/starred{/owner}{/repo}",
            "subscriptions_url": "https://api.github.com/users/Ada-Developers-Academy/subscriptions",
            "organizations_url": "https://api.github.com/users/Ada-Developers-Academy/orgs",
            "repos_url": "https://api.github.com/users/Ada-Developers-Academy/repos",
            "events_url": "https://api.github.com/users/Ada-Developers-Academy/events{/privacy}",
            "received_events_url": "https://api.github.com/users/Ada-Developers-Academy/received_events",
            "type": "Organization",
            "site_admin": false
        },
        "private": false,
        "html_url": "https://github.com/Ada-Developers-Academy/LessonPlanning",
        "description": null,
        "fork": false,
        "url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning",
        "forks_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/forks",
        "keys_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/keys{/key_id}",
        "collaborators_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/collaborators{/collaborator}",
        "teams_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/teams",
        "hooks_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/hooks",
        "issue_events_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/issues/events{/number}",
        "events_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/events",
        "assignees_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/assignees{/user}",
        "branches_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/branches{/branch}",
        "tags_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/tags",
        "blobs_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/git/blobs{/sha}",
        "git_tags_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/git/tags{/sha}",
        "git_refs_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/git/refs{/sha}",
        "trees_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/git/trees{/sha}",
        "statuses_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/statuses/{sha}",
        "languages_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/languages",
        "stargazers_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/stargazers",
        "contributors_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/contributors",
        "subscribers_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/subscribers",
        "subscription_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/subscription",
        "commits_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/commits{/sha}",
        "git_commits_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/git/commits{/sha}",
        "comments_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/comments{/number}",
        "issue_comment_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/issues/comments{/number}",
        "contents_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/contents/{+path}",
        "compare_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/compare/{base}...{head}",
        "merges_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/merges",
        "archive_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/{archive_format}{/ref}",
        "downloads_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/downloads",
        "issues_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/issues{/number}",
        "pulls_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/pulls{/number}",
        "milestones_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/milestones{/number}",
        "notifications_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/notifications{?since,all,participating}",
        "labels_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/labels{/name}",
        "releases_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/releases{/id}",
        "deployments_url": "https://api.github.com/repos/Ada-Developers-Academy/LessonPlanning/deployments",
        "created_at": "2013-06-13T14:56:27Z",
        "updated_at": "2016-08-01T01:50:17Z",
        "pushed_at": "2013-10-31T01:43:27Z",
        "git_url": "git://github.com/Ada-Developers-Academy/LessonPlanning.git",
        "ssh_url": "git@github.com:Ada-Developers-Academy/LessonPlanning.git",
        "clone_url": "https://github.com/Ada-Developers-Academy/LessonPlanning.git",
        "svn_url": "https://github.com/Ada-Developers-Academy/LessonPlanning",
        "homepage": null,
        "size": 1607,
        "stargazers_count": 17,
        "watchers_count": 17,
        "language": "Ruby",
        "has_issues": true,
        "has_projects": true,
        "has_downloads": true,
        "has_wiki": true,
        "has_pages": false,
        "forks_count": 22,
        "mirror_url": null,
        "archived": false,
        "open_issues_count": 4,
        "license": null,
        "forks": 22,
        "open_issues": 4,
        "watchers": 17,
        "default_branch": "master",
        "permissions": {
            "admin": false,
            "push": false,
            "pull": true
        }
    },
    {
      // second repo
    }
    // additional repos
]
````