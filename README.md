# California Accountability Panel documentation

Documentation for the [California Accountability Panel website](https://github.com/opensacorg/app-capanel-web).

## Prerequisites

- [uv](https://docs.astral.sh/uv/)
- [pnpm](https://pnpm.io/)
- [Make](https://opensacorg.github.io/app-capanel-doc/developer_guide#install)

## Quickstart

Get started with building and running the documentation. Useful commands can be run with Make; see [Makefile](/Makefile). **If you have any issues with Make, try to run the corresponding application manually.** 

### Backend

Documentation for the general application and Python code uses Sphinx. This is where most of the documentation should be. For more information, see the [Sphinx documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/sphinx).

#### Create an `.env` file.

To run the main FastAPI application, first create an `.env` file in the root of the repository. This step can be skipped if you just want to build/run the documentation.

```dotenv
# Domain
# This would be set to the production domain with an env var on deployment
# used by Traefik to transmit traffic and aqcuire TLS certificates
DOMAIN=localhost
# To test the local Traefik config
# DOMAIN=localhost.tiangolo.com

# Used by the backend to generate links in emails to the frontend
FRONTEND_HOST=http://localhost:5173
# In staging and production, set this env var to the frontend host, e.g.
# FRONTEND_HOST=https://dashboard.example.com

# Environment: local, staging, production
ENVIRONMENT=local

PROJECT_NAME="California Accountability Panel"
STACK_NAME=full-stack-fastapi-project

# Backend
BACKEND_CORS_ORIGINS="http://localhost,http://localhost:5173,https://localhost,https://localhost:5173,http://localhost.tiangolo.com"
SECRET_KEY=changethis
FIRST_SUPERUSER=admin@example.com
FIRST_SUPERUSER_PASSWORD=changethis

# Emails
SMTP_HOST=
SMTP_USER=
SMTP_PASSWORD=
EMAILS_FROM_EMAIL=info@example.com
SMTP_TLS=True
SMTP_SSL=False
SMTP_PORT=587

# Postgres
POSTGRES_SERVER=localhost
POSTGRES_PORT=5432
POSTGRES_DB=app
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres

SENTRY_DSN=

# Configure these with your own Docker registry images
DOCKER_IMAGE_BACKEND=backend
DOCKER_IMAGE_FRONTEND=frontend
```

#### Live-reload the Sphinx documentation.

Build the backend documentation and start a local server on [localhost:8000](localhost:8000).

```shell
make reload
```

### Frontend

The frontend documentation uses Storybook. For more information, see the [Storybook documentation](https://opensacorg.github.io/app-capanel-doc/developer-guide/storybook).

```shell
make storybook
```

## Contribute

You can get involved by joining our Meetup group and Slack channel. For more information on contributing to the project, see the [contribution guide](https://opensacorg.github.io/app-capanel-doc/contribute).
