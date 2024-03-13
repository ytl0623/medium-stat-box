<p align="center">
   <img src="https://i.imgur.com/lTFt1CF.png" alt="screenshot" width="500">
  <h3 align="center">📌 Medium Stat Box</h3>
</p>

<p align="center">
   <img src="https://img.shields.io/badge/language-typescript-blue?style"/>
   <img src="https://img.shields.io/github/stars/kylemocode/medium-stat-box"/>
</p>
<p align="center">
   Show your medium stat 😁
   <br/>
   Including followers count and the title and claps of your latest articles
</p>

> This project is inspired by many projects collected in [awesome-pinned-gists](https://github.com/matchai/awesome-pinned-gists)

> You can see example in my [github pinned projects](https://github.com/kylemocode)

## Breaking Change

update at 2022/04/21.

Because medium change their website's structure, the old version of this gist do not work, please pull the latest version of this action.

## Overview

This project uses Medium RSS API to get personal profile data and uses cheerio to crawl more details such as follower count and claps of articles. The following details will be displayed in pinned gist:

- Medium username and number of followers
- Latest 3 articles and their claps count

> warning: medium articles with no categories will be filtered

## Setup

### Prep work

1. Create a new public GitHub Gist (https://gist.github.com/)
2. Create a token with the `gist` scope and copy it. (https://github.com/settings/tokens/new)

### Project setup

1. Fork this repo
2. Go to the fork repo's **Actions** tab to enable workflow in fork repo
![image](https://github.com/ytl0623/medium-stat-box/assets/55120101/94664c43-b0ce-47e5-a014-10b12e0b766b)

4. Go to the fork repo's **Settings > Secrets**
![image](https://github.com/ytl0623/medium-stat-box/assets/55120101/a3b4e01f-5217-4d97-b655-d721de9b9bbc)

6. Add the following environment variables:

   - **GH_PAT:** The personal access token generated above.
   - **GIST_ID:** The ID portion from your gist url:
     ex: https://gist.github.com/kylemocode/ **44ccec1f7d16680a7a42a2e91a2d0d4c**
   - **MEDIUM_USER_NAME:** The user name of your medium account
     ex: https://medium.com/@ **oldmo860617**

7. [Pin your gist](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/pinning-items-to-your-profile)
8. Wait for it to update (the github aciton cron job will run every 8 hours), or you can manually push the repo to trigger the action.

## Change Log

`2021/10/14` : Update crawler regex for followers
