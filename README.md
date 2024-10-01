# 2024-09-23 this repository is outdated and is no longer maintained

We've moved the development of the Helm chart to a private VCS and repo. Please refer to the documentation pages for correct links and instructions.
[Please use the documentation pages instead](https://docs.qameta.io/allure-testops/install/docker-compose/)


# Allure TestOps version 5, configuration files for docker compose installation

## Configuration sets

1. testops-demo
2. testops
3. testops-ldap
4. testops-saml

### testops-demo

Config `testops-demo` **cannot be used** as production deployment. Use this as a proof of concept or demo for the decision making.

Demo config contains all the components required for the starting Allure TestOps up, however this configuration requires a lot of maintenance and will lead to significant downtime and possible data loss when database upgrade is required.

We won't be able to help with data restoration or performance issues when Allure TestOps is deployed with demo config.

### testops

Use this configuration if you are going to manage end users and their authentication via Allure TestOps UI (so-called local users or system authentication).

#### Target deployment architecture

| Component      | Deployed as                  |
|----------------|------------------------------|
| Allure TestOps | via docker compose           |
| Postgres       | standalone server            |
| RabbitMQ       | preferably standalone server |
| Redis          | preferably standalone server |
| S3 solution    | standalone server            |

### testops-ldap

Use this configuration if you are going to manage end users and their authentication via existing LDAP server.

#### Target deployment architecture

| Component      | Deployed as                  |
|----------------|------------------------------|
| Allure TestOps | via docker compose           |
| Postgres       | standalone server            |
| RabbitMQ       | standalone server            |
| Redis          | preferably standalone server |
| S3 solution    | standalone server            |

### testops-saml

Use this configuration if you are going to manage end users and their authentication via existing Identity Provider service supporting SAML2 authentication.

#### Target deployment architecture

| Component      | Deployed as                  |
|----------------|------------------------------|
| Allure TestOps | via docker compose           |
| Postgres       | standalone server            |
| RabbitMQ       | preferably standalone server |
| Redis          | preferably standalone server |
| S3 solution    | standalone server            |

### testops-openid

Use this configuration if you are going to manage end users and their authentication via existing Identity Provider service supporting OpenID authentication.

#### Target deployment architecture

| Component      | Deployed as                  |
|----------------|------------------------------|
| Allure TestOps | via docker compose           |
| Postgres       | standalone server            |
| RabbitMQ       | preferably standalone server |
| Redis          | preferably standalone server |
| S3 solution    | standalone server            |

## Upgrade from version 4 to version 5

The only available paths from to upgrade 4 to 5  are

- 4.26.5 → 5.3.3 and next releases

Upgrade process is thoroughly described in [Allure TestOps documentation here.](https://)
