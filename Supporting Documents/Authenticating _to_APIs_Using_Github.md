# Overview
This exercise guides students on how to authenticate API requests using GitHub’s Personal Access Tokens (PAT) and perform basic actions like retrieving user information and repositories using curl commands.

### Prerequisites:
- GitHub account and command line tool access(cURL).
- A PAT (see below)

## Generate a Personal Access Token (PAT)
Follow these steps to generate a Personal Access Token:

1. Log in to GitHub and navigate to **Settings > Developer settings > Personal access tokens**.
2. Click **Generate new token**, then add a description like "API Exercise Token."
3. Select the repo and user scopes to allow API access to user and repository information.
4. Generate and **save the token securely**, as it’s only shown once.

For more information, check the [Authenticating with a Personal Access Token](https://docs.github.com/en/rest/authentication/authenticating-to-the-rest-api?apiVersion=2022-11-28#authenticating-with-a-personal-access-token).

# GETing information
Below will be steps on how to make GET requests against an endpoint that requires authentication using your PAT

## Retrieve User Information
First lets retrieve it from a public endpoint so you can see the difference

### Retrieve Information about a Specific User (Public Profile)
Use curl to retrieve information about a specific GitHub user by their username. This example retrieves information about the octocat user, a public GitHub test account.
```bash
curl https://api.github.com/users/octocat
```
**Expected Output:** A JSON response containing public profile details of octocat, including their ID, profile image URL, bio, and other public metadata.
Pay close attention to the response where it says:
```bash
{...
"user_view_type": "public",
...}
```

### Retrieve Authenticated User Information
Using `curl`, make a `GET` request to the `/user` endpoint to retrieve information about your GitHub user account. This request requires authentication with your PAT. Replace **YOUR_TOKEN** with your token(PAT).
```bash
curl -H "Authorization: Bearer <YOUR_TOKEN>" https://api.github.com/user
```
**Expected Output:** A JSON response with private and public details about your GitHub profile, such as your username, email (if public), and bio.This endpoint provides a more comprehensive view than the public user endpoint, as it returns additional information available only with authentication.

Pay close attention to the response where it says:
```bash
{...
"user_view_type": "private",
...}
```

## Retrieve Repo Information
### Retrieve Your Repositories
Retrieve a list of your GitHub repositories by making a GET request to the /user/repos endpoint. This also requires authentication with your PAT.
```bash
curl -H "Authorization: Bearer <YOUR_TOKEN>" https://api.github.com/user/repos
```
**Additional Exploration:**
Try different authenticated requests with other GitHub endpoints, such as:
- Listing followers: https://api.github.com/user/followers
- Listing organizations: https://api.github.com/user/orgs

# Sending information(POST)
## POST a Request to Create a New Repository
Use `curl` to send a `POST` request that creates a new repository in your GitHub account. The following example will create a repository named `test-api-repo` with a description and a choice of public visibility.
```bash
curl -X POST -H "Authorization: Bearer <YOUR_TOKEN>" \
-H "Accept: application/vnd.github+json" \
-d '{"name": "test-api-repo", "description": "A repository created via GitHub API", "private": false}' \
https://api.github.com/user/repos
```
Replace **YOUR_TOKEN** with your actual token.

**Payload Explanation:**

- **"name":** The name of the new repository (e.g., "test-api-repo").
- **"description":** A brief description of the repository.
- **"private":** Set to false to make the repository public; set to true for private.


**Expected Output:** A JSON response with details of the newly created repository, including the repository URL.
<details>
<summary>Example Response Expand source </summary>
  
  ```json
  {
  "id": 886935195,
  "node_id": "R_kgDONN2Omw",
  "name": "test-api-repo",
  "full_name": "tamalerhino/test-api-repo",
  "private": false,
  "owner": {
    "login": "tamalerhino",
    "id": 34582172,
    "node_id": "MDQ6VXNlcjM0NTgyMTcy",
    "avatar_url": "https://avatars.githubusercontent.com/u/34582172?v=4",
    "gravatar_id": "",
    "url": "https://api.github.com/users/tamalerhino",
    "html_url": "https://github.com/tamalerhino",
    "followers_url": "https://api.github.com/users/tamalerhino/followers",
    "following_url": "https://api.github.com/users/tamalerhino/following{/other_user}",
    "gists_url": "https://api.github.com/users/tamalerhino/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/tamalerhino/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/tamalerhino/subscriptions",
    "organizations_url": "https://api.github.com/users/tamalerhino/orgs",
    "repos_url": "https://api.github.com/users/tamalerhino/repos",
    "events_url": "https://api.github.com/users/tamalerhino/events{/privacy}",
    "received_events_url": "https://api.github.com/users/tamalerhino/received_events",
    "type": "User",
    "user_view_type": "public",
    "site_admin": false
  },
.....
  ```
</details>

### Verify the New Repository on GitHub
After making the `POST` request, navigate to your GitHub account to view the new repository in your repository list. You should see it with the name, description, and visibility you specified in the request.

# Sending More information
Again everything is a request, so first you sent a request to the server to give you information using the GET HTTP Method, then you used the POST HTTP Method to send a request with information you are providing to create the repo. Next we will send the server another request to delete the repo we just made. This could be done using a POST request depending on the server, but HTTP does provide us with a method specifically for deleting this, ideally most web applications are architected to use the most common HTTP methods and usually align to CRUD methodology.

## Send a DELETE Request to Remove the Repository
Use the `DELETE` `HTTP` method to remove the `test-api-repo` repository from your GitHub account. The format for this request is as follows:

- Replace YOUR_TOKEN with your GitHub token.
- Replace YOUR_USERNAME with your GitHub username.
```bash
curl -X DELETE -H "Authorization: token YOUR_TOKEN" \
https://api.github.com/repos/YOUR_USERNAME/test-api-repo
```

**Expected Output:** If the request is successful, there will be no JSON response, indicating the repository was deleted successfully. If the repository does not exist or permissions are incorrect, an error message will appear.

### Verification
After sending the`DELETE` request, refresh your GitHub profile to confirm that `test-api-repo` is no longer listed in your repositories.

## Summary
In these exercises, we explored the differences between `authenticated` and `unauthenticated` API calls, as well as the use of various HTTP methods (`GET`, `POST`, and `DELETE`). Unauthenticated calls allow access to public data, like viewing a GitHub user’s public profile, but are limited in functionality and rate limits. Authenticated calls, on the other hand, require a Personal Access Token (PAT) and enable access to private data, higher rate limits, and the ability to perform actions like creating or deleting resources. We used `GET` requests to retrieve data (e.g., user profiles and repositories), `POST` requests to create resources (such as a new repository), and `DELETE` requests to remove resources (like deleting that repository). Together, these concepts demonstrated how authentication provides secure access and control over resources, while different HTTP methods define the type of action we want to perform within an API

## References
Reference Links:
- [User Endpoint Documentation](https://docs.github.com/en/rest/users?apiVersion=2022-11-28)
- [Repository Endpoint Documentation](https://docs.github.com/en/rest/repos?apiVersion=2022-11-28)
- [Getting Started with the REST API Guide](https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api?apiVersion=2022-11-28&tool=curl)
