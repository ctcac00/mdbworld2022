# MongoDB World 2022

One Server(less) to Worry About: How to Build a Complete Serverless Back End with MongoDB Atlas

This is the Realm application used in the demonstration

## Prerequisites

- A MongoDB [Atlas account](http://cloud.mongodb.com)
- A MongoDB [Atlas serverless instance](https://www.mongodb.com/developer/how-to/atlas-serverless-quick-start) named **serverlesss-mdb**
- MongoDB [Realm CLI](https://www.mongodb.com/docs/realm/cli/) installed on your laptop

## How to deploy

- Log-on to your [Atlas account](http://cloud.mongodb.com)

- Navigate to the project you are using and go to the API Keys tab on the [Access Management](https://docs.atlas.mongodb.com/configure-api-access#manage-programmatic-access-to-a-project) page.

- **Generate** a new **Programmatic API Key**

- Now on your laptop's console, log-on to your Atlas account:

```bash
realm-cli login --api-key="ATLAS-API-PUBLIC-KEY" --private-api-key="ATLAS-API-PRIVATE-KEY"
```

- Now import the application accepting the defaults in the import wizard:

```bash
realm-cli push --local "./mdbworld-1"
```

> **_NOTE:_** If there is an error in the import process, manually delete the Realm application and try again. A common issue is that the cluster name does not match the default **serverlesss-mdb**

You should see a success message similar to:

```bash
Successfully imported 'mdbworld-1-<EMPTY>'
```

> **_NOTE:_** Notice that the identifier will be empty, and you will have to retrieve it from the Realm app configuration page.
