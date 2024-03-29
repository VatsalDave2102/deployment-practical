# deployment-practical
This repo contains examples of different builds i.e. Development, Production, Staging
## Production build
**Production build**: A production build is optimized for performance and is intended to be used in a live production environment. It typically includes optimizations like code minification, tree shaking, and image compression to reduce file size and improve page load times. The importance of a production build lies in providing a fast and responsive website or application that delivers a good user experience to users.
Below linked site is the production build site. 

**Link**: https://practical-6-production-build.netlify.app/

For local: 

**Environment Variable**: Environment variables are a way to pass configuration information to an application at runtime, without hardcoding the values in the code. They are typically set in the operating system or container environment and are accessible to the application as key-value pairs.

I have created a .env.production to access the environment variable named VITE_REACT_APP_BUILD
```
VITE_REACT_APP_BUILD='THIS IS PRODUCTION BUILD'
```
I am accessing it in App.jsx to display the value:
```
import.meta.env.VITE_REACT_APP_BUILD
```
**Note**: To access env variables in code when using Vite, define it with prefix **'VITE_'** or else variable won't be accessible. 

This branch is deployed on Netlify and I have added environment variable there as well, as we must should keep .env files untracked from git.

The build command in package.json is :
```
"build": "vite build"
```
This will generate a dist folder in your project directory that contains the production-ready files for your app.

To run production build on local server: 

Install a static file server such as serve or http-server using the following command:
```
npm install -g serve
```

This will install the serve package globally on your machine.

Navigate to the dist folder using the following command:

``` 
cd dist
```
Start the static file server using the following command:

```
serve -s
```
