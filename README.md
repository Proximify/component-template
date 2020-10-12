# Component Template

Template for the creation of component packages.

<!-- The TOC can be provided inline as nested bullets or in a separate file. Regardless, this starter file should have links to other root-level doc files so that a reader can navigate all the documentation by reading the text and clicking on hyperlinks within it. -->

-   [Table of contents](docs/toc.md)

## Getting started

1. Download this repo manually from GitHub.
1. Change the name of the root folder to reflect the name of your component (use a CamelCase name).
1. Edit the composer.json to set the proper name of your component package (use lowercase, dash separated words).
1. Renamed the main PHP and JSON files to the CamelCase name of the component.
1. Edit the README and files under `docs/` to include the documentation for your component. Use breadcrumbs at the top of each doc page to show its location in the Table of Contents (TOC). Keep the `toc.md` file up to date with the latest TOC of your documentation.
1. If the packages depends of foreign packages (e.g. NPM, PIP, etc), use the [ForeingPackages](https://packagist.org/packages/proximify/foreign-packages) component to install and update them when your component is installed or updated.
1. Add CLI actions for testing your component bu using the [CLI Actions](https://packagist.org/packages/proximify/cli-actions) component.
1. If possible to test your component within a webpage, add an `index.php` file at `dev/www` and test that it works by running `cd dev/www && php -S localhost:8000` and visiting `http://localhost:8000` with your browser.
1. Submit your project to **Packagist** of it is public and test that it works by adding it as a requirement to some other project.

## File Structure

A **component package** is a folder with a standardized file structure.

The **entry point** file must be place under a `src` folder at the root of the package. It must be a class definition where the class name is the module name. There file should only define one class and should not run any code. The constructor of the class should accept an `array $options = []` argument where the **named** arguments needed to create an object are provided.

The **Composer project name** is always lowercase and with no spaces. The convention is to fill spaces with dashes. In addition, a namespace is mandatory. For example,

    proximify/my-component

In contrast, the **component name** is given as a single word in CamelCase with a name space also in CamelCase. For example,

    Proximify\MyComponent

The **short or unqualified component name** is thee component name within its namespace. Similarly, the **short or unqualified project name** is the name of the project without its namespace.

The typical file structure of a component package is:

```
# Project name: proximify/my-component

MyComponent
├── assets
│   ├── images
│   │   └── example.svg
│   └── fonts
├── docs
│   └── intro.md
├── settings
│   └── MyComponent.json
├── src
│   └── MyComponent.php
├── dev
│   ├── tests
│   └── www
├── LICENSE
├── README.md
└── composer.json
```

**Note:** Everything related to development and testing should be placed under the `dev` folder. The component should work in production without that folder.

---

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to and actually do, grant us the rights to use your contribution. For details, visit our [Contributor License Agreement](https://github.com/Proximify/community/blob/master/docs/proximify-contribution-license-agreement.pdf).

When you submit a pull request, we will determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided. You will only need to do this once across all repositories using our CLA.

This project has adopted the [Proximify Open Source Code of Conduct](https://github.com/Proximify/community/blob/master/docs/code_of_conduct.md). For more information see the Code of Conduct FAQ or contact support@proximify.com with any additional questions or comments.

## License

Copyright (c) Proximify Inc. All rights reserved.

Licensed under the [MIT](https://opensource.org/licenses/MIT) license.

**Software component** is made by [Proximify](https://proximify.com). We invite the community to participate.
