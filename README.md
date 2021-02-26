Clone (use --recurse-submodules)

```
git clone --recurse-submodules GITHUB_URL
```

Check out a given branch (and the corresponding commits at each submodule)

```
git checkout --recurse-submodules --force develop
```

Now you need to install, link and locally build the packages linked by lerna.

```
npm run bootstrap
```

```
cd js-uprtcl
npm run build
cd ..
```

Now you should run the [Web Server](https://github.com/uprtcl/js-uprtcl-server/tree/develop) (Check it's README file, but you need to create an `.env` file and run dgraph with docker);

Finally you can run the consuming application which uses the libraries and connects to the Web Server.

```
cd linked-thoughts
touch src/services/env.ts
```

And fill it with the following content:

```ts
export const env = {
  // host: 'https://api.intercreativity.io/uprtcl/1',
  host: 'http://localhost:3100/uprtcl/1',
};
```

Then run the app in dev mode

```
cd linked-thoughts
npm run dev
```

Now open `localhost:8002` on your browser and you should see the application. Use Metamask to login as Auth0 access is limited to an oklist.
