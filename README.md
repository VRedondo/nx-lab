# Nx Lab
### Project Structure

The structure of the project is based on packages, libs.

```
packages
├── [domain]
	├──[app-name]
libs
├── [domain]
	├──[app-name]
└── shared
```

Where 
- packages contains all applications, these needs to be group by a specific domain
- libs contain services, components, utilities, etc. They have well-defined public API. It's a good convention to put applications-specific libraries into the directory matching the application name. This provides enough organization for small to mid-size applications.

## Nx generators

Generators provide a way to automate many tasks you regularly perform as part of your development workflow. Whether it is scaffolding out components, features, ensuring libraries are generated and structured in a certain way, or updating your configuration files, generators help you standardize these tasks in a consistent, and predictable manner.
Check the [official Nx packages available](https://nx.dev/plugin-features/use-code-generators#invoking-plugin-generators) docs for information regarding their generators and add them as a convenience.

The plugins `@nrwl/next @nrwl/nest` were already set to generate scaffolding applications for Front-End app with NextJS and Back-End app with NestJS.

### Generate a NextJS or Nest scaffolding apps

Open a terminal at the root level of the monorepo and run 

For NextJS
```
nx g @nrwl/next:app [application-name] --style=styled-components --directory=[path]
```

For NestJS
```
nx g @nrwl/nest:app [application-name] --directory=[path]
```

By default all the applications are going to be created under the `packages` folder, replace the brakets placeholders for the proper values.

## Nx IDE Integration

It's recommended to download and install Nx console integration plugin in your IDE, currently there are 2 integrations available for VSCode and JetBrains, check it it [here](https://nx.dev/core-features/integrate-with-editors).

### TBD