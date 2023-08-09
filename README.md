
<p align="center">
  <img src="https://authress.io/static/images/logo-text-200.png" height="100px" alt="Authress logo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://localstack.cloud/images/header-logo-new.svg" height="85px" alt="LocalStack logo">

</p>

# LocalStack Extension for Authress Authentication and Authorization

This is the [LocalStack](https://localstack.cloud/) extension that enables running authentication, user identity, permissions, api key management, and access control in your [LocalStack environment](https://localstack.cloud/) via [Authress](https://authress.io).

This LocalStack extension generates a copy of the [Authress API](https://authress.io/app/#/api) so that the authentication and access management the Authress API provides can be utilized by running services directly in any environment. You can use this to build authentication and authorization directly into your applications and services. Additionally, this extension can be used locally to develop faster without needing an [Authress Account](https://authress.io).

<p align="center">
    <a href="https://badge.fury.io/py/localstack-extension-authress" alt="LocalStack Authress Extension">
        <img src="https://badge.fury.io/py/localstack-extension-authress.svg">
    </a>
    <a href="https://github.com/Authress/localstack-extension/actions/workflows/build.yml" alt="Build status">
      <img src="https://github.com/Authress/localstack-extension/actions/workflows/build.yml/badge.svg">
    </a>
    <a href="https://github.com/Authress/localstack-extension/blob/main/LICENSE" alt="Apache-2.0">
      <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg">
    </a>
    <a href="https://authress.io/community" alt="authress community">
      <img src="https://img.shields.io/badge/Community-Authress-fbaf0b.svg">
    </a>
</p>

===============================

## Installation

To install the Authentication & Authorization extension into LocalStack, run
```sh
localstack extensions install localstack-extension-authress
```

## Usage
The auth extension runs at `http://authress.localhost.localstack.cloud:8888`.

You can configure API calls to the authorization server by passing this url as the `authressApiUrl` or the `authress_api_url` depending on which SDK you are using.


```ts
import { AuthressClient } from 'authress-sdk';
const authressClient = new AuthressClient({ authressApiUrl: `http://authress.localhost.localstack.cloud:8888` });
await authressClient.userPermissions.authorizeUser(userId, resourceUri, permission);
```

## Knowledge Base

Review the in depth guides in the [Authress Local KB](https://authress.io/knowledge-base/docs/SDKs/authress-local).

## Contribution Guide

[Developing for the LocalStack Authress Extension](https://github.com/Authress/localstack-extension/blob/main/contributing.md)