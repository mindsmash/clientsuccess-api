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
`clientsuccess.clients.list(params)`
#### Create
`clientsuccess.clients.create(params)` 
#### Read
`clientsuccess.clients.read(clientId, params)`
#### Update
`clientsuccess.clients.update(clientId, params)`
#### Delete
`clientsuccess.clients.delete(clientId, params)`

### Contacts

#### List
`clientsuccess.contacts.list(clientId, params)`
#### Create
`clientsuccess.contacts.create(clientId, params)`
#### Read
`clientsuccess.contacts.read(clientId, contactId, params)`
#### Delete
`clientsuccess.contacts.delete(clientId, contactId, params)`

### Contact Custom Fields
`clientsuccess.contactCustomFields(params)` 

### Interactions

#### List
`clientsuccess.interactions.list(clientId, params)`
#### Create
`clientsuccess.interactions.create(clientId, params)`
#### Update
`clientsuccess.interactions.update(clientId, interactionId, params)`
#### Delete
`clientsuccess.interactions.delete(clientId, interactionId, params)`

### Todos

#### List
`clientsuccess.todos.list(clientId, params)`
#### Create
`clientsuccess.todos.create(clientId, params)`
#### Update
`clientsuccess.todos.read(clientId, todoId, params)`
#### Delete
`clientsuccess.todos.delete(clientId, todoId, params)`

### Pulses

#### List
`clientsuccess.pulses.list(clientId, params)`
#### Create
`clientsuccess.pulses.create(clientId, params)`

### Employees
`clientsuccess.employees(params)`

### Products

#### List
`clientsuccess.products.list(params)`
#### Create
`clientsuccess.products.create(params)`
#### Read
`clientsuccess.products.read(productId, params)`
#### Update
`clientsuccess.products.update(productId, params)`
#### Delete
`clientsuccess.products.delete(productId, params)`

### Client Types
`clientsuccess.clientTypes(params)`

### Client Statuses
`clientsuccess.clientStatuses(params)`

### Subscriptions
`clientsuccess.subscriptions(params)`
