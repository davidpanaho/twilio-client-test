# Twilio Client test repro

This is a minimum repro of a potential issue with the Twilio JS client package.

## Installation

Install the packages by running:

```
npm install
```

Build the JS files for inspection by running:

```
npm run build
```

This will run both the default Webpack builder and Parcel builder. The built files can be found in the following locations:

- Webpack: `dist/main.js`
- Parcel: `dist/index.js`

## Potential issues

- If you build this on your local machine, you should be able to find the file path to this project in the built files by searching for `_where`.
- the built files also show the registry from which you've downloaded the Twilio package by searching for `_resolved`. This is mainly an issue if you're using a private repository as it exposes an IP address/domain.
