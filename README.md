# Client Success
A 3rd party node.js library that implements the [ClientSuccess](https://www.clientsuccess.com/) API.

[Documentation](http://docs.clientsuccessapi.apiary.io/#reference)

## Instalation
```bash
npm i clientsuccess-api
```

## Usage

This library uses [axios](https://github.com/mzabriskie/axios) to send HTTP request. All methods will expose the underlying `config` parameter for `axios`

Begin by initializing with your username and password. 

```javascript
let clientsuccess = require('clientsuccess-api').clientsuccess(username, password);
```

Now you will be able to interact with the Client Success API. This API will handle refreshing your access token.
Client Success [reccomends](http://help.clientsuccess.com/advanced-features/does-clientsuccess-have-an-api) that you create a seperate user account named "API Access"

```javascript
clientsuccess.clients.list()
  .then(response => console.log(response))
  .catch(err => console.log(err));
```

## Methods

### Clients

#### List
#### Create
#### Read
#### Update
#### Delete

### Contacts

#### List
#### Create
#### Read
#### Delete

### Contact Custom Fields

### Interactions

#### List
#### Create
#### Update
#### Delete

### Todos

#### List
#### Create
#### Update
#### Delete

### Pulses

#### List
#### Create

### Employees

### Products

#### List
#### Create
#### Read
#### Update
#### Delete

### Client Types

### Client Statuses

### Subscriptions
