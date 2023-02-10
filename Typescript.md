# Typesctipt

## Resources
https://www.typescriptlang.org/
https://www.tutorialsteacher.com/typescript

- Install Typescript globally
````
npm i -g typescript
````

- Check Typescript version
````
tsc -v
````

- Generate `.js` from `.ts` (here `first.ts` is just an example `.ts` file).
This generates automatically `ES3` standard `JS` file
````
tsc first.ts
````

- The way to override `ES` version on generating `JS` code
````
tsc --target es6 first.js
````

- To define target once for project add to `tsconfig.json`
````
{
    "compilerOptions": {
        "target": "ES6"
    }
}
````

- In order to execute Typescript code against NodeJS we need to set up `TS`
execution environment for NodeJs. So it's needed to install `ts-node` package
globally
````
npm i -g ts-node
````

- Execute Typescript code from terminal
````
node first.ts
````
or
````
ns-node first.ts
````

- Webpack and Yarn are alternative package managers