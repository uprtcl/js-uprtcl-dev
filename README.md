A simple lerna.json and package.json configuration to develop @uprtcl libraries

- checkout the packages monorepo

```
git clone git@github.com:uprtcl/js-uprtcl.git
```

create a folder for the testing app

```
mkdir apps
cd apps
git clone git@github.com:uprtcl/demo-simple.git
cd demo-simple
npm run update-uprtcl
```

The last command should make sure the app is using the latest @uprtcl versions. Most of our apps include it.

Now go bacl to the root folder where lerna.json is and chose which packages you want lerna to link in lerna.json -> packages.

And run them in dev mode (this will hot reload the packages and the app)

```
lerna bootstrap
npm run dev
```
