# React Project

## Steps to build and deploy on gh-pages

1. Comment build folder in .gitignore file. So that we can push the build folder to gh-pages
2. Add the following 2 lines in package.json to set the PUBLIC_URL and push build content to gh-pages 

The value of PUBLIC_URL should be your git repository name which you want to publish

Note: PUBLIC_URL=/YOUR_GIT_REPO_NAME/ 

```js
"gh-build": "PUBLIC_URL=/react-project/ npm run build",
"gh-pages": "npm run gh-build && git subtree push --prefix build origin gh-pages"
```
3. Commit your code and push your changes to master or main branch
4. Run the command `npm run gh-pages`
5. You should be able to access the published site in few seconds.
6. Try to access the URL `https://<YOUR_GIT_USERNAME>.github.io/<YOUR_GIT_REPO_NAME>/`
7. Example `https://rajkeshwar.github.io/react-project/`



