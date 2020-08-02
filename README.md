# This template has been merged back into the [official halogen template](https://github.com/purescript-halogen/purescript-halogen-template/). Use that template instead for the latest development recommendations.


### Quick Start
```
git clone https://github.com/purescript-templates/halogen.git myApp
cd myApp
npm install -g purescript spago parcel
npm run build
npm run serve
```

### Introduction

This template for [purescript-halogen v5](https://github.com/purescript-halogen/purescript-halogen) mimics the introductory example of the [official React Hooks documentation](https://reactjs.org/docs/hooks-intro.html).

Additional documentation for halogen can be found here:
* [Official guide](https://github.com/purescript-halogen/purescript-halogen/tree/master/docs)
* [Learn-halogen repo](https://github.com/JordanMartinez/learn-halogen/)
* [Real World Halogen](https://github.com/thomashoneyman/purescript-halogen-realworld) - The published article is written for the older halogen v4, but the code and comments cover the current halogen v5.

Pursuit docs are not published yet, but you can build documentation locally with `spago docs` then open `generated-docs/html/index.html`.

More examples are available in the [package repository](https://github.com/purescript-halogen/purescript-halogen/tree/master/examples).

If you notice any problems with the below setup instructions, or have suggestions on how to make the new-user experience any smoother, please create an issue or pull-request.

Compatible with PureScript compiler 13.6

### Initial Setup

Install tools globally:
```
npm install -g purescript spago parcel
```
Initial compilation:
```
npm run build
```
Launch webapp:
```
npm run serve
```

### Development Cycle
If you're using an [editor](https://github.com/purescript/documentation/blob/master/ecosystem/Editor-and-tool-support.md#editors) that supports [`purs ide`](https://github.com/purescript/purescript/tree/master/psc-ide) or are running [`pscid`](https://github.com/kRITZCREEK/pscid), you simply need to keep the previous `npm run serve` command running in a terminal. Any save to a file will trigger an incremental recompilation, rebundle, and web page refresh, so you can immediately see your changes.

If your workflow does not support automatic recompilation, or if you add, remove, or modify module names, then you will need to manually re-run `npm run build`.

### Production

When you are ready to create a minified bundle for deployment, run the following command:
```
npm run build-prod
```

Parcel output appears in the `./dist/` directory.

You can test the production output locally with a tool like [`http-server`](https://github.com/http-party/http-server#installation). It seems that `parcel` should also be able to accomplish this, but it unfortunately will only serve development builds locally.
```
npm install -g http-server
http-server dist -o
```

If everything looks good, you can then upload the contents of `dist` to your preferred static hosting service.

### Local Versioned Toolchain

If you'd prefer to install tools on a per-project basis (rather than globally) see [this guide](https://github.com/purescript-templates/docs/blob/master/versioned-toolchain.md).
