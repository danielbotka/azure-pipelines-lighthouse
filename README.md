# Lighthouse for Azure Pipelines

This is an Azure DevOps extension that allows you to enhance your build and release pipelines with a new Lighthouse tab.
The Lighthouse tab embed the HTML report generated by [Google Lighthouse](https://developers.google.com/web/tools/lighthouse/).

The extension comes with a task that requires:
- The URL of the website to analyse,
- The npm package [lighthouse](https://www.npmjs.com/package/lighthouse) installed on your agent, either locally or globally.

The task also allows you to specify audit rules that can make the pipeline fail based on the audit scores.

For example, the Google Lighthouse audit `no-vulnerable-libraries` has a boolean score that will be equal to 0 if there are known vulnerabilities within client-side JavaScript libraries and frameworks detected on a web site.
In order to make the pipeline fail if this audit score is not equal to 1, you can type:

```
no-vulnerable-libraries = 1
```

You can also use the `>` (greater than) operator to evaluate audit scores that are decimal between 0 and 1.

## Screenshots

![Lighthouse HTML report embed in a tab](https://raw.githubusercontent.com/sharegate/azure-pipelines-lighthouse/master/docs/lh-result.png?v0)

![Lighthouse task](https://raw.githubusercontent.com/sharegate/azure-pipelines-lighthouse/master/docs/lh-task.png?v0)

## Installation

Lighthouse for Azure Pipelines is not yet available on the Visual Studio Marketplace.

## Usage

N/A

## Compiling

N/A

## License

Copyright © 2018, Groupe Sharegate inc. This code is licensed under the Apache License, Version 2.0. You may obtain a copy of this license at https://github.com/sharegate/azure-pipelines-lighthouse/blob/master/LICENSE.
