## Lesson 3: Extending CI/CD 

### Contributions

The GitHub actions used as default CI/CD workflow in a Firefly App are leveraging:

* `adobe/aio-cli-setup-action` used to install and configure the [CLI](https://github.com/adobe/aio-cli) on the GitHub infrastructure running the workflow that invoked the action. 
* `adobe/aio-apps-action` centralizes the support for a GitHub workflow to leverage several application specific commands, such as testing via `aio app test` and deployment via `aio app deploy`.

They can also be used further in custom GitHub workflows built by developers to fulfil their project needs.

Both actions have been published and can be found on the GitHub Marketplace. See [CLI Setup](https://github.com/marketplace/actions/aio-cli-setup) and [Apps](https://github.com/adobe/aio-apps-action).

All submissions should come in the form of pull requests and need to be reviewed by project committers. 
We do our best to keep on top of all the pull requests. We may suggest some changes, improvements or alternatives.

### Custom CI/CD workflow

The default implementation of the CI/CD workflow for Project Firefly Applications relies on GitHub capabilities. However, a developer might need an alternative solution due to project specific requirements, or team preference.

In that case, we recommend implementing the custom solution with focus on two main aspects:

* The [CLI](https://github.com/adobe/aio-cli) is the official tool to manage the Project Firefly Application development lifecycle from bootstrapping to deployment, and can be used within a CI/CD workflow for automation purpose.
* Security is a key requirement, and any alternative CI/CD workflow should propose a solid secret management solution to store the credentials required to deploy a Project Firefly Application against a specific **Workspace**.

Next: [Well done](welldone.md) 