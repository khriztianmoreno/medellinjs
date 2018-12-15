# mde-js-site
[![All Contributors](https://img.shields.io/badge/all_contributors-10-orange.svg?style=flat-square)](#contributors)

> MedellinJS Website powered by NuxtJS

## Build Setup

Check your Node version, this must be higher that 8+.

``` bash
$ node -v
#v8.11.1

# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).

## Creating a Pull Request

There are 2 main work flows when dealing with pull requests:

1. Pull Request from a [forked repository](https://help.github.com/articles/fork-a-repo)
2. Pull Request from a branch within a repository

Here we are going to focus on 1.

### Creating a Feature Branch

After making a fork of this repository to your account.

First create a branch with a characteristic name of the work you are going to do, example: `admin-page`, `mobile-version`. Make sure your repository is up to date first using

```bash
$ git checkout develop
$ git pull origin develop
```

*Note:* `git pull` does a `git fetch` followed by a `git merge` to update the local repo with the remote repo. For a more detailed explanation, see [this stackoverflow post](http://stackoverflow.com/questions/292357/whats-the-difference-between-git-pull-and-git-fetch).

To create a branch, use `git checkout -b <new-branch-name> [<base-branch-name>]`, where `base-branch-name` is optional and defaults is current branch `develop`. I'm going to create a new branch called `pull-request-demo` from the `master` branch and push it to github.

```bash
git checkout -b pull-request-demo
git push origin pull-request-demo
```

### Creating a Pull Request

To create a pull request, you must have changes committed to your new branch.

Go to the repository page on github. And click on "Pull Request" button in the repo header.

**Note**: You must do the Pull Request on the `develop` branch.

If you have questions you can see more information in the following link [Creating a pull request](https://help.github.com/articles/creating-a-pull-request/)

## External API usage

### Meetups

This site uses the meetup.com API to pull the past and next events for the MedellinJS group. All requests to the API are JSONP request signed with an API Key, which is the only supported mode if you dont want to use OAuth (requires user approval), or reval your API key in the source code (which should only used be on server side apps).

The only endpoint hitted to pull the events is the [V3 Group events](https://www.meetup.com/meetup_api/docs/:urlname/events/#list) endpoint, which is used to pull both upcoming events and past events.

Signed requests can be generated from the [Meetup API Console](https://www.meetup.com/meetup_api/console/) and can only be used for the specific resource involved. Because the signed requests carry the identity of the user that generated them, its recommended to use them only for read-only requests without side effects (GET).

JSONP needs to be used because the meetup API only supports CORS headers on requests that use OAuth authentication. [See github issue](https://github.com/meetup/api/issues/130).

For further information about the meetup API please check the [documentation](https://www.meetup.com/meetup_api/).

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/733877?v=4" width="100px;"/><br /><sub><b>Julian Duque</b></sub>](http://about.me/julianduque)<br />[💻](https://github.com/coljs/medellinjs/commits?author=julianduque "Code") [📋](#eventOrganizing-julianduque "Event Organizing") [📢](#talk-julianduque "Talks") [👀](#review-julianduque "Reviewed Pull Requests") [📝](#blog-julianduque "Blogposts") | [<img src="https://avatars1.githubusercontent.com/u/1189785?v=4" width="100px;"/><br /><sub><b>Adrián Estrada</b></sub>](https://github.com/edsadr)<br />[💻](https://github.com/coljs/medellinjs/commits?author=edsadr "Code") [📋](#eventOrganizing-edsadr "Event Organizing") [📢](#talk-edsadr "Talks") [👀](#review-edsadr "Reviewed Pull Requests") [📝](#blog-edsadr "Blogposts") | [<img src="https://avatars3.githubusercontent.com/u/1482473?v=4" width="100px;"/><br /><sub><b>Alex Ramirez</b></sub>](http://twitter.com/RamirezAlex_)<br />[📋](#eventOrganizing-RamirezAlex "Event Organizing") [📢](#talk-RamirezAlex "Talks") | [<img src="https://avatars0.githubusercontent.com/u/1205255?v=4" width="100px;"/><br /><sub><b>Jesse cogollo</b></sub>](http://jessecogollo.me/)<br />[📋](#eventOrganizing-jessecogollo "Event Organizing") [💻](https://github.com/coljs/medellinjs/commits?author=jessecogollo "Code") [📖](https://github.com/coljs/medellinjs/commits?author=jessecogollo "Documentation") [💵](#financial-jessecogollo "Financial") [👀](#review-jessecogollo "Reviewed Pull Requests") [📢](#talk-jessecogollo "Talks") | [<img src="https://avatars1.githubusercontent.com/u/1481964?v=4" width="100px;"/><br /><sub><b>Khriztian Moreno</b></sub>](http://khriztianmoreno.com/)<br />[💻](https://github.com/coljs/medellinjs/commits?author=khriztianmoreno "Code") [📖](https://github.com/coljs/medellinjs/commits?author=khriztianmoreno "Documentation") [👀](#review-khriztianmoreno "Reviewed Pull Requests") [📢](#talk-khriztianmoreno "Talks") [🐛](https://github.com/coljs/medellinjs/issues?q=author%3Akhriztianmoreno "Bug reports") [🎨](#design-khriztianmoreno "Design") | [<img src="https://avatars2.githubusercontent.com/u/14205513?v=4" width="100px;"/><br /><sub><b>Maria Fernanda Serna Arboleda</b></sub>](http://mafesernaarboleda.co/)<br />[📋](#eventOrganizing-mafesernaarboleda "Event Organizing") [📢](#talk-mafesernaarboleda "Talks") [🔍](#fundingFinding-mafesernaarboleda "Funding Finding") | [<img src="https://avatars1.githubusercontent.com/u/2567952?v=4" width="100px;"/><br /><sub><b>Jeny Alejandra Mazo</b></sub>](https://github.com/JenyMzo)<br />[💻](https://github.com/coljs/medellinjs/commits?author=JenyMzo "Code") [🎨](#design-JenyMzo "Design") [📋](#eventOrganizing-JenyMzo "Event Organizing") [💵](#financial-JenyMzo "Financial") [📢](#talk-JenyMzo "Talks") |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [<img src="https://avatars3.githubusercontent.com/u/9942486?v=4" width="100px;"/><br /><sub><b>Frank Alejo Betancur</b></sub>](https://github.com/Krank2me)<br />[📋](#eventOrganizing-Krank2me "Event Organizing") [📢](#talk-Krank2me "Talks") | [<img src="https://avatars1.githubusercontent.com/u/545352?v=4" width="100px;"/><br /><sub><b>Ely Alvarado</b></sub>](https://github.com/elyalvarado)<br />[💻](https://github.com/coljs/medellinjs/commits?author=elyalvarado "Code") | [<img src="https://avatars2.githubusercontent.com/u/3019827?v=4" width="100px;"/><br /><sub><b>CodeMaxter</b></sub>](https://github.com/CodeMaxter)<br />[📋](#eventOrganizing-CodeMaxter "Event Organizing") [📢](#talk-CodeMaxter "Talks") |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
