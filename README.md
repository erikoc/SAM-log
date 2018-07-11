# SAM-log

## Usage
The default settings should make sure that no initialisation of the library is needed for Omnicar's applications.
The only **Prerequisite** to make if default to what we usually use for log level is having the `NODE_ENV` environment variable available.

Another option is to have the `LOG_LEVEL` environment variable available (has to be one of: `error` | `warn` | `info` | `verbose` | `debug` | `silly`) which will set the loglevel directly.

To use the library, simply import the log function needed. E.g. `logError` and use it like a regular call to `console.error`.

It's possible to use an optional prefix for all the logging methods. The available logging methods are:

* `logError(message: string | object, prefix: string = '', meta?: any | any[])`
* `logWarn(message: string | object, prefix: string = '', meta?: any | any[])`
* `logInfo(message: string | object, prefix: string = '', meta?: any | any[])`
* `logVerbose(message: string | object, prefix: string = '', meta?: any | any[])`
* `logDebug(message: string | object, prefix: string = '', meta?: any | any[])`

## Developing

Pull the project, run `yarn` and you should be good.

Before you do a `git push`, please run `yarn tsc-once` to generate the build folder contents.

## Testing

There are a bunch of `jest` tests in the `index.test.ts` file. Run `yarn test` to run all tests, `yarn test-watch` to run them in watch-mode, and run `yarn test-debug` to run them in watch mode with `--inspect` enabled (allowing you to step debug).