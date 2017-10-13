![Estonian Information System Authority](https://github.com/e-gov/RIHA-Frontend/raw/master/logo/gov-CVI/lions.png "Estonian Information System Authority") ![European Regional Development Fund](https://github.com/e-gov/RIHA-Frontend/raw/master/logo/EU/EU.png "European Regional Development Fund")

# RIHA-help
RIHA help files for UI and API end-users


## Steps to finish

1. Enable [Travis](https://docs.travis-ci.com/user/getting-started/#To-get-started-with-Travis-CI%3A) for your repository (**note**: you already have `.travis.yml` file)
2. [Create GitHub access token](https://help.github.com/articles/creating-an-access-token-for-command-line-use/); check `public_repo` on `Select scopes` section.
3. Use the token value as a value for [Travis environment variable](https://docs.travis-ci.com/user/environment-variables/#Defining-Variables-in-Repository-Settings) with the name `GH_TOKEN`
4. Make a test commit to trigger CI: `git commit --allow-empty -m "Test Travis CI" && git push`
5. Wait until Travis build is finished. You can check progress by clicking on the `Build Status` badge at the top
6. If you did everything correct, https://kertuhiire.github.io/RIHA-Help/ will lead to your new docs
7. **[Optional]** You can setup [custom domain](https://help.github.com/articles/using-a-custom-domain-with-github-pages/) (just create `web/CNAME` file)
8. Start writing/editing your OpenAPI spec: check out [usage](#usage) section below
9. **[Optional]** If you document public API consider adding it into [APIs.guru](https://APIs.guru) directory using [this form](https://apis.guru/add-api/).
10. Delete this section :smile:

## Links

- Documentation(ReDoc): https://kertuhiire.github.io/RIHA-Help/
- SwaggerUI: https://kertuhiire.github.io/RIHA-Help/swagger-ui/
- Look full spec:
    + JSON https://kertuhiire.github.io/RIHA-Help/swagger.json
    + YAML https://kertuhiire.github.io/RIHA-Help/swagger.yaml
- Preview spec version for branch `[branch]`: https://kertuhiire.github.io/RIHA-Help/preview/[branch]

**Warning:** All above links are updated only after Travis CI finishes deployment

## Working on specification
### Install

1. Install [Node JS](https://nodejs.org/)
2. Clone repo and `cd`
    + Run `npm install`

### Usage

1. Run `npm start`
2. Checkout console output to see where local server is started. You can use all [links](#links) (except `preview`) by replacing https://kertuhiire.github.io/RIHA-Help/ with url from the message: `Server started <url>`
3. Make changes using your favorite editor or `swagger-editor` (look for URL in console output)
4. All changes are immediately propagated to your local server, moreover all documentation pages will be automagically refreshed in a browser after each change
**TIP:** you can open `swagger-editor`, documentation and `swagger-ui` in parallel
5. Once you finish with the changes you can run tests using: `npm test`
6. Share you changes with the rest of the world by pushing to GitHub :smile:
