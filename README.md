# California Accountability Panel documentation

Documentation for the California Accountability Panel website. https://github.com/opensacorg/app-capanel-web


The general application and Python documentation uses Sphinx. This is where most of the documentation should be. For more information, see the [Sphinx documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/sphinx). The frontend documentation uses [Storybook](https://opensacorg.github.io/app-capanel-doc/developer-guide/storybook).

## Prerequisites

- [uv](https://docs.astral.sh/uv/)
- [pnpm](https://pnpm.io/)
- [Make](https://opensacorg.github.io/app-capanel-doc/developer_guide#install)

## Quickstart

This project supports VSCode and Make. **If you have any issues with these commands, try to run the corresponding application individually with uv or pnpm.** 

### Create an `.env` file.

To run the main FastAPI application, first create an `.env` file in the root of the repository. For all of the options, see the [environment variable documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/environment-variable). This step can be skipped if you just want to build/run the documentation.

```dotenv
FIRST_SUPERUSER=admin@example.com
FIRST_SUPERUSER_PASSWORD=changethis
POSTGRES_SERVER=localhost
POSTGRES_USER=postgres
```

### VSCode

Enable the workspace recommended extensions before running a launch command. For all of the options, see the [VSCode support documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/vscode)

- Run the frontend and backend application.

### Make

For all of the options, see the [Make support documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/vscode)

#### Build and launch the Sphinx documentation.

Live-reload the backend documentation and start a local server on [localhost:8000](localhost:8000).

```shell
make reload
```

You can also use:

```shell
make html
make preview
```

#### Build and launch the Storybook documentation.

```shell
make storybook
```

## Contribute

You can get involved by joining our Meetup group and Slack channel. For more information on contributing to the project, see the [contribution guide](https://opensacorg.github.io/app-capanel-doc/contribute).
