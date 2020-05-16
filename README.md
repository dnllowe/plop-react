# React Code Creator

## Summary
Create boilerplate code for common React files.

React Code Creator is a simple implementation of [plop.js](https://plopjs.com/) for common React files.

React Code Creator supports creating the following types of React files:
* Views (`jsx` or `tsx`)
* Services
* Contexts
* Models (when using typescript)
* Includes `css` and test `spec` files

## Install
`npm install react-code-creator`

Or

`yarn add react-code-creator`

## Using

### Config file
React Code Creator uses a `react-code-creator.config.yaml` file (which you should place at your project's root directory) to determine how to generate certain files. The config file should automatically be added to your root folder after installation with npm.

The config file has the following properties:

```yaml
useTypescript: # Default: false
generateCss: # Default: true
generateTests: # Default: true
cssExtension: # Default: "css"
testExtension: # Default: "spec"
root: # Default: "./src"
viewPath: # Default "views"
modelPath: # Default "models"
servicePath: # Default "services"
contextPath: # Default "contexts"
fileCase: # Default "camel"
pathCase: # Default "camel"
```

|Property|Description|Possible Values|Default|
|--------|-----------|---------------|-------|
|useTypescript|Whether to create typescript files (`.tsx`, `.ts`)|`true` or `false`|`false`|
|generateCss|Whether to generate css files when creating components|`true` or `false`|`true`|
|generateTests|Whether to generate test spec files when creating components and services|`true` or `false`|`true`|
|cssExtension|Define the type of css file to generate|`"css"`, `"scss"`, `"less"`, `"sass"`|`"css"`|
|testExtension|The file extension for test spec files|`"spec"` or `"test"`|`"spec"`|
|root|The root directory for your source code (where React Code Creator will place the generated files)|any filepath string|`"./src"`|
|viewPath|Where in the `root` directory to place autogenerated views|any filepath string|`"views"`|
|modelPath|Where in the `root` directory to place autogenerated models|any filepath string|`"models"`|
|servicePath|Where in the `root` directory to place autogenerated services|any filepath string|`"services"`|
|contextPath|Where in the `root` directory to place autogenerated contexts|any filepath string|`"contexts"`|
|fileCase|Casing type to try and enforce when creating file names|`"camel"`, `"pascal"`, `"dash"`, `"snake"`, `"dot"`|`"camel"`|
|pathCase|Casing type to try and enforce when creating file paths|`"camel"`, `"pascal"`, `"dash"`, `"snake"`|`"camel"`|

### Casing Examples (fileCase and pathCase)
* camel: camelCaseNames
* pascal: PascalCaseNames
* dash: dash-case-names
* snake: snake_case_names
* dot: dot.case.names

### Running
After installing, React Code Creator should add a `new` script to your `package.json` file.

Run `npm run new` to begin the CLI

### Skipping prompts
If you already know the values you would like to provide the CLI, you can add them as args

For example: `npm run new componenent myComponent`

### Commands
You can see the full list of commands by running `npm run new`

### Changing the Run command
You can change the command from `new` by updating the `scripts` section of your `package.json` file.