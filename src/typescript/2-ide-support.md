@page learn-typescript/ide-support IDE Support
@parent learn-typescript 2

@description Learn about TypeScript configurations and IDES good for TypeScript Development.

@body

## Overview

In this section we'll learn about TypeScript configuration options to help us optimize our workflow, and look at IDEs that have great TypeScript support for building TypeScript projects.

For the exercise, we will learn how to import and export functions between modules.

## Configuring TypeScript

We're able to configure how our projects use TypeScript from selecting which files to compile to removing comments from those files. This is done through the creation of a ``tsconfig.json`` file.

### tsconfig.json

Customize the TypeScript compiling and linting options by creating a ``tsconfig.json`` file in the root directory of your TypeScript project. The following config will
- specify ECMAScript target version as 'es5'
- specify module code generation (from 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015' or 'esnext')
- generate source map files
- remove comments from compiled code

The following is just example config code. __Don't add this to your project or the tests for the TypeScript exercises in this training will fail.__

```javascript
{
    "compilerOptions": {
        "target": "es5",
        "module": "commonjs",
        "sourceMap": true,
        "removeComments": true
    }
}
```

Full configuration options are available here: <a href="http://json.schemastore.org/tsconfig" target="\_blank">http://json.schemastore.org/tsconfig</a>

### Linting

We can also configure linting options to catch bugs and help enforce uniform styling. The following options will warn on unused local variables and parameters, and expressions or declarations implying 'any'.

```javascript
{
    "compilerOptions": {
        ...
        "noUnusedLocals": true,
        "noUnusedParameters": true,
        "noImplicitAny": true
        ...
	}
}
```

## IDEs

Integrated Development Environments have come a long way in supporting modern web development. With little to no configuration IDEs offer built-in debugging, Git integration, command line usage, and robust packages for additional add-ons.

### Visual Studio Code

<a href="https://code.visualstudio.com/" target="\_blank">VS Code</a> is Microsoft's modern take on an IDE for app development (P.S. TypeScript is a Microsoft Open Source project).  VS Code has built in TypeScript support for syntax highlighting, IntelliSense code completion, and linting.

<a href="../static/img/vs-code-screenshot.png" target="\_blank"><img src="../static/img/vs-code-screenshot.png" width="100%" alt="Visual Studio Code screenshot" /></a>

### Atom

Atom is another good modern IDE that easily supports and aids in TypeScript development with the installation of the <a href="https://atom.io/packages/atom-typeScript" target="\_blank"> atom-typeScript plugin</a>.

<a href="../static/img/atom-screenshot.png" target="\_blank"><img src="../static/img/atom-screenshot.png" width="100%" alt="Atom screenshot" /></a>

### Webstorm

<a href="https://www.jetbrains.com/webstorm/download/" target="\_blank">Webstorm</a> is a platform by JetBrains that is loved for its great code refactoring assistance and version control integration, but it does require a paid subscription.

<a href="../static/img/webstorm-screenshot.png" target="\_blank"><img src="../static/img/webstorm-screenshot.png" width="100%" alt="Webstorm screenshot" /></a>

## Exercise: Exporting and Importing

### The Problem

In this exercise, we will:

- Update _1-ide-greeter.ts_ to export the `greeter` function as the `default`
  export. _1-ide-greeter.ts_ currently looks like:
  ```ts
  function greeter(person: string) {
    return "Hello, " + person;
  }
  ```
- Update _1-ide-hello-earth.ts_, to import and use `greeter`. _1-ide-hello-earth.ts_ currently looks like:
  ```ts
  document.body.innerHTML = greeter("Earth");
  ```
- Compile _1-ide-hello-earth.ts_ to JavaScript so we can run it.

### What You Need to Know

- [Export](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) a default value like:
  ```typescript
  const value:string = "My Value";
  export default value;
  ```
- [Import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) a default value like:
  ```typescript
  import value from "./value-exporter";
  ```

### Verify Your Solution

✏️ Run the following to verify your solution works:

```shell
npm run 1-ide
```

### The Solution

<details>
<summary>Click to see the solution</summary>
✏️ Update `1-ide-greeter.ts` to:

```typescript
function greeter(person: string) {
	return "Hello, " + person;
}

export default greeter;
```
@highlight 5

✏️ Update `1-ide-hello-earth.ts` to:

```typescript
import greeter from './1-ide-greeter';

document.body.innerHTML = greeter("Earth");
```
@highlight 1

✏️ Compile `1-ide-hello-earth.ts` with:

```shell
tsc 1-ide-hello-earth.ts
```

</details>

### Things to Explore

- Hover over `greeter`, what does your IDE show?
- Pass a number to `greeter`, what does your IDE show?
