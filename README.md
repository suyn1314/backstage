![headline](docs/headline.png)

# [Backstage](https://backstage.io)

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![](https://github.com/spotify/backstage/workflows/Frontend%20CI/badge.svg)
[![Discord](https://img.shields.io/discord/687207715902193673)](https://discord.gg/EBHEGzX)
![Code style](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)
[![](https://img.shields.io/npm/v/@backstage/core?label=Version)](https://github.com/spotify/backstage/releases)

## What is Backstage?

[Backstage](https://backstage.io/) is an open platform for building developer portals. Powered by a centralized service catalog, Backstage restores order to your microservices and infrastructure. So your product teams can ship high-quality code quickly — without compromising autonomy.

Backstage unifies all your infrastructure tooling, services, and documentation to create a streamlined development environment from end to end.

![service-catalog](https://backstage.io/blog/assets/6/header.png)

Out of the box, Backstage includes:

- [Backstage Service Catalog](https://github.com/spotify/backstage/blob/master/docs/features/software-catalog/index.md) for managing all your software (microservices, libraries, data pipelines, websites, ML models, etc.)
- [Backstage Software Templates](https://github.com/spotify/backstage/blob/master/docs/features/software-templates/index.md) for quickly spinning up new projects and standardizing your tooling with your organization’s best practices
- [Backstage TechDocs](https://github.com/spotify/backstage/tree/master/docs/features/techdocs) for making it easy to create, maintain, find, and use technical documentation, using a "docs like code" approach
- Plus, a growing ecosystem of [open source plugins](https://github.com/spotify/backstage/tree/master/plugins) that further expand Backstage’s customizability and functionality

For more information go to [backstage.io](https://backstage.io) or join our [Discord chatroom](https://discord.gg/EBHEGzX).

## Project roadmap

We created Backstage about 4 years ago. While our internal version of Backstage has had the benefit of time to mature and evolve, the first iteration of our open source version is still nascent. We are envisioning three phases of the project and we have already begun work on various aspects of these phases:

- 🐣 **Phase 1:** Extensible frontend platform (Done ✅) - You will be able to easily create a single consistent UI layer for your internal infrastructure and tools. A set of reusable [UX patterns and components](http://storybook.backstage.io) help ensure a consistent experience between tools.

- 🐢 **Phase 2:** Service Catalog ([alpha released](https://backstage.io/blog/2020/06/22/backstage-service-catalog-alpha)) - With a single catalog, Backstage makes it easy for a team to manage ten services — and makes it possible for your company to manage thousands of them. Developers can get a uniform overview of all their software and related resources, regardless of how and where they are running, as well as an easy way to onboard and manage those resources.

- 🐇 **Phase 3:** Ecosystem (later) - Everyone's infrastructure stack is different. By fostering a vibrant community of contributors we hope to provide an ecosystem of Open Source plugins/integrations that allows you to pick the tools that match your stack.

Check out our [Milestones](https://github.com/spotify/backstage/milestones) and open [RFCs](https://github.com/spotify/backstage/labels/rfc) how they relate to the three Phases outlined above.

Our vision for Backstage is for it to become the trusted standard toolbox (read: UX layer) for the open source infrastructure landscape. Think of it like Kubernetes for developer experience. We realize this is an ambitious goal. We can’t do it alone. If this sounds interesting or you'd like to help us shape our product vision, we'd love to talk. You can email me directly: [alund@spotify.com](mailto:alund@spotify.com).

## Overview

The Backstage platform consists of a number of different components:

- **app** - Main web application that users interact with. It's built up by a number of different _Plugins_. This repo contains an example implementation of an app (located in `packages/app`) and you can easily get started with your own app by [creating one](docs/getting-started/create-an-app.md).
- [**plugins**](https://github.com/spotify/backstage/tree/master/plugins) - Each plugin is treated as a self-contained web app and can include almost any type of content. Plugins all use a common set of platform API's and reusable UI components. Plugins can fetch data either from the _backend_ or through any RESTful API exposed through the _proxy_.
- [**service catalog**](https://github.com/spotify/backstage/tree/master/packages/backend) - Service that holds the model of your software ecosystem, including organisational information and what team owns what software. The backend also has a Plugin model for extending its graph.
- [**proxy**](https://github.com/spotify/backstage/tree/master/plugins/proxy-backend) - Terminates HTTPS and exposes any RESTful API to Plugins.
- **identity** - A backend service that holds your organisation's metadata.

## Getting started

To run a Backstage app, you will need to have the following installed:

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [NodeJS](https://nodejs.org/en/download/) - Active LTS Release, currently v12
- [yarn](https://classic.yarnpkg.com/en/docs/install)

After cloning this repo, open a terminal window and start the example app using the following commands from the project root:

```bash
yarn install # Install dependencies

yarn start # Start dev server, use --check to enable linting and type-checks
```

The final `yarn start` command should open a local instance of Backstage in your browser, otherwise open one of the URLs printed in the terminal.

And that's it! You are good to go 👍

### Next step

Take a look at the [Getting Started](docs/getting-started/index.md) guide to learn how to set up Backstage, and how to develop on the platform.

## Documentation

- [Main documentation](docs/README.md)
- [Service Catalog](docs/features/software-catalog/index.md)
- [Create a Backstage App](docs/getting-started/create-an-app.md)
- [Architecture](docs/overview/architecture-terminology.md) ([Decisions](docs/architecture-decisions/index.md))
- [Designing for Backstage](docs/dls/design.md)
- [Storybook - UI components](http://storybook.backstage.io)

## Contributing

We would love your help in building Backstage! See [CONTRIBUTING](CONTRIBUTING.md) for more information.

## Community

- [Discord chatroom](https://discord.gg/MUpMjP2) - Get support or discuss the project
- [Good First Issues](https://github.com/spotify/backstage/contribute) - Start here if you want to contribute
- [RFCs](https://github.com/spotify/backstage/labels/rfc) - Help shape the technical direction
- [FAQ](docs/FAQ.md) - Frequently Asked Questions
- [Code of Conduct](CODE_OF_CONDUCT.md) - This is how we roll
- [Adopters](ADOPTERS.md) - Companies already using Backstage
- [Blog](https://backstage.io/blog/) - Announcements and updates
- [Newsletter](https://mailchi.mp/spotify/backstage-community)
- Give us a star ⭐️ - If you are using Backstage or think it is an interesting project, we would love a star ❤️

Or, if you are an open source developer and are interested in joining our team, please reach out to [foss-opportunities@spotify.com ](mailto:foss-opportunities@spotify.com)

## License

Copyright 2020 Spotify AB.

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
