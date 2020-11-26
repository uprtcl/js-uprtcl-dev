A simple lerna and package.json configuration to develop @uprtcl libraries

- checkout the packages you want to modify

```
git clone git@github.com:uprtcl/js-uprtcl-core.git
git clone git@github.com:uprtcl/js-uprtcl-connections.git
git clone git@github.com:uprtcl/js-uprtcl-modules.git
git clone git@github.com:uprtcl/js-uprtcl-remotes.git
```

create a folder for the testing app

```
mkdir apps
cd apps
git clone git@github.com:uprtcl/intercreativity-react.git
```

chose which packages you want lerna to link in lerna.json -> packages.

And run them in dev mode (this will hot reload the packages and the app)

```
lerna bootstrap
lerna run dev --parallel
```
